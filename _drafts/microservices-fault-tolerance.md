---
layout: post
title: "Microservices lessons - fault tolerance"
metaTitle: "Microservices challenges and lessons from trenches"
description: "This post is part of the microservices lessons series. In this post I talk about challenges of fault tolerance in microservices and provide a few practical tips on how you can deal with failures"
date: "2015-08-15"
permalink: "/presentations/microservices-lessons-dddmel"
tags: ["Microservices", "Architecture"]
---

This post is part of the [microservices lessons series](/microservices-lessons).

Fault Tolerance is normally mentioned as one of the benefits of microservices architecture because in theory if you have loosely coupled services, the failure in one shouldn't impact the rest of the application while in a monolithic application when a server goes down, it takes the entire application down with it. I have been involved in quite a few distributed projects and majority of them were much less fault tolerant than their equivalent monolithic application.

Let's do the math: let's say we have 30 services, which isn't too many for a medium sized microservices architecture, each with 99.9% uptime, which is quite an impressive up-time! The total downtime of all the services put together is 1296 minutes a month. That is 21.6 hours. Now if you isolate the failures in each service properly, your system could actually be available 100% of the time; but if you don't do that, failure in each service could ripple through your system and bring down your entire application: this means around one day of downtime a month! Not very impressive, is it? And unfortunately this is not so uncommon in distributed systems!!

Let me give you an example from a project I worked on. We were using [Akamai](https://en.wikipedia.org/wiki/Akamai_Technologies), *one of the world's largest Content Delivery Solution responsible for serving between 15 to 30 percent of all web traffic*, in a project. As a developer you don't expect Akamai to fail frequently, and that was an assumption we made. We were happily making a blocking call to Akamai to persist an image as part of a user initiated transaction. Everything was sweet until one day vast majority of interactions with the website started crashing, and all failing because the calls to Akamai were failing! Funnily Akamai was up and running. We soon learnt that you can't store more than 10,000 files in one directory in Akamai and we had reached that limit and from that point on all the transactions were being rejected. Now this was an external service; but regardless we hadn't isolated the failures and that issue cost the business a fair bit of money.

### Contain the failure
As mentioned before, you must contain the failure on a service or it could bring down the rest of the system with it. There two main integration patterns in a distributed architecture: RESTful and messaging. Some services would benefit from RESTful pattern and some interactions are best implemented with messaging.

>> Note: Traditionally request/response services were implemented using RPC pattern which you would execute a remote procedure on a service. RPC style integration is now considered rather outdated and most request/response integrations are now modeled as RESTful services, and in this post I'm focusing on RESTful services.

#### Contain the failure in a RESTful interaction
For your services that use request/response pattern, a useful pattern to isolate the failure is the Circuit Breaker Pattern. If you want to learn more about this pattern, I would recommend you to read Martin Fowler's [post](http://martinfowler.com/bliki/CircuitBreaker.html) on it.

The idea behind circuit breaker is that if one of your services or components is struggling, hammering it with more requests is not going to help it recover. So you put a failure threshold, say 5 failing hits in a row, and when that threshold is reached, you stop hitting the component (opening the circuit) to give it some time to recover and wait in the open state for a predefined time. After that, you change the state to half-open which lets one transaction through to see if the service's back up again. If yes, you close the circuit and things are back to normal, and if not, you open the circuit again, this time potentially with a longer timeout.

So circuit breaker helps the failing system recover, but what is the consumer supposed to do in the open state? Because if you're not getting the response you need, you might still be failing!

If what you're after is some data, as in you're making a GET request, you could use fallbacks. In a typical microservices architecture, you will end up with some data duplication across services to avoid chatty communication between services. That means there's a chance another service might have the response you're after! If so, perhaps hit that service in the meantime to resolve the response you're after. Alternatively, and if it makes sense to the transaction you're processing, perhaps you can use cache successful responses, and then upon the failure server the last successful response for that request!

If fallback is not an option, either because you don't have that data on another service or you can't return stale data, then you should consider graceful degradation. You can return a canned response when a service is down, maybe a Null Response, and implement your consuming services to understand the Null Response and gracefully degrade the user experience.

#### Contain the failure using messaging
If you want the other service to take some actions, then fallbacks don't help because you need those services to do something. In this case, a message bus is your friend. Instead of waiting for that service to respond to your request you can just fire a message that gets queued somewhere when the service is down and as soon as the service comes up the message is delivered. The service can then process the transaction. This leads into [CAP theorem and eventual consistency](http://www.allthingsdistributed.com/2007/12/eventually_consistent.html), which I will ignore in this post/talk.
