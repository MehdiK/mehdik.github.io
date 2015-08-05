---
layout: post
title: "Microservices lessons from trenches"
metaTitle: "Microservices challenges and lessons from trenches"
description: "There has been a bit of hype lately around microservices and all you hear is how awesome microservices architecture is. This series is about challenges: things you don't normally hear when developers talk about microservices"
date: "2015-08-05"
tags: ["Microservices", "Architecture"]
---

There has been a bit of hype lately around microservices. You go to conferences and read blogs and all you hear is how awesome microservices architecture is. Some of the main (perceived) benefits of microservices are:

 - Scalability: unlike monolithic apps, you can scale the services that actually need to scale instead of the whole app.
 - Loose coupling: loosely coupled services can be versioned (or rewritten from the ground up) independently without impacting the rest of the system.
 - Fault tolerance: due to loose coupling, isolated processes and hosting, faults in one service doesn't impact the rest of the system.
 - Scalable development: you can't throw 50 developers on one codebase as that would lead to a lot of merge conflicts; but you could throw 50 developers at 10 repositories without any problems.
 - Lower cognitive load: instead of having 1 million lines of entangled code in one repository, each service has its own repository which is a lot lighter. That means you can wrap your head around a service end to end a lot simpler.
 - Technical diversification: since you have different codebase and data storage for each service, you can use the best tool for the job in each service: use relational DB for one service and graph DB for another, use Node for one service and Java for another etc.
 - Autonomous teams: each service typically has a service team that owns it, from perception and design all the way to implementation and hosting. Ideally a service team has complete autonomy over the service: they get to pick the technology they want to use and implement the way it makes sense to them, as opposed to having to follow a single coding standard and tech stack which is typical of monolithic applications.
 - Continuous delivery: it's a lot simpler to do continuous delivery of smaller independent services and components than to continuously release an entire application all at once. Loose coupling and fault tolerance also make it easier to deploy frequently without impacting the entire system.
 - Evolutionary design: smaller services are easier to create, change and evolve and that facilitates experimentation. Create a service to validate an idea. If it flies, keep it and evolve it, and if not, kill it. To do this effectively you will need deployment and infrastructure automation.

I purposely didn't go into details of these benefits because they've been written and talked about many times. If you're interested you can learn more about microservices and their benefits and challenges [here](http://martinfowler.com/microservices/).

I love microservices and distributed systems and that's my main expertise - what I don't like is the hype. Good developers are very passionate about what they do, and they hear or see something awesome, and they're blinded by the passion and desire to try the latest and shiniest and suddenly they HAVE to do it, not because it fits their needs but because they like to try it. So, this series is not about the benefits of microservices - it's about its challenges: things you don't normally hear when developers talk about microservices.

Here is an (evolving) index of posts I am considering to write over time:

  - Culture
  - Fault tolerance
  - Loose coupling
  - Greenfield microservices
  - Service size and boundaries
  - Continuous delivery
  - Decentralized data management
  - REST or messaging?

I hope that by highlighting some of these challenges, you weigh the challenges and cost of microservices against its benefits before you pick it for your next project.

Stay tuned!
