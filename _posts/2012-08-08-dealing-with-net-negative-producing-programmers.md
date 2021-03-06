--- 
layout: post
title: "Dealing with Net Negative Producing Programmers"
metaTitle: "Dealing with Net Negative Producing Programmers"
description: "Net Negative Producing Programmers are those who insert enough spoilage to exceed the value of their production"
revised: "2012-08-11"
date: "2012-08-08"
tags: ["Productivity","Team","Notes","Rants"]
migrated: "true"
permalink: "/dealing-with-net-negative-producing-programmers"
summary: "

"
---
In his '[Productivity Variations Among Software Developers and Teams](http://blogs.construx.com/blogs/stevemcc/archive/2008/03/27/productivity-variations-among-software-developers-and-teams-the-origin-of-quot-10x-quot.aspx)' post Steve McConnell mentions:

<blockquote>Researchers have found 10-fold differences in productivity and quality between different programmers with the same levels of experience and also between different teams working within the same industries</blockquote>

But the difference seems a lot more than that. Those studies must have missed or overlooked something! Oh wait, here is an interesting bit further down on Steve's post:

<blockquote>In several of the published studies on software productivity, about 10% of the subjects in the experiments weren't able to complete the experimental assignment. In the studies, they writeups say, "Therefore those experimental subjects' results were excluded from our data set."</blockquote>

So those figures are not indicative of what goes on in the industry and as Steve says:

<blockquote>in real life if someone "doesn't complete the assignment" you can't just "exclude their results from the data set." You have to wait for them to finish, assign someone else to do their work, and so on. The interesting (and frightening) implication of this is that something like 10% of the people working in the software field might actually be contributing *negative* productivity to their projects.</blockquote>

In fact there are a lot of programmers who contribute negatively to their team and project. G. Gordon Schulmeyer came up with a great name for these programmers: [Net Negative Producing Programmer](http://www.pyxisinc.com/NNPP_Article.pdf) (AKA NNPP):

<blockquote>We've known since the early sixties, but have never come to grips with the implications that there are net negative producing programmers (NNPPs) on almost all projects, who insert enough spoilage to exceed the value of their production.</blockquote>

Most NNPPs work slowly. It takes them a long time to do a simple task and the time it takes them to complete a task exponentially grows as the task gets harder. They also produce some really buggy result. According to Gordon:

<blockquote>The ratio of programmer performance that repeatedly appeared in the studies investigated by Bill Curtis in the July/August 1990 issue of American Programmer was 22 to 1.  This was both for source lines of code produced and for debugging times - which includes both defect detection rate and defect removal efficiency. [5, pp. 4 - 6]  The NNPP also produces a higher instance of defects in the work product. </blockquote>

They are not net negative because they do not work - if they did not work and/or were a passive employee they would just have zero productivity. They are net negative for a few reasons. For example for some NNPPs you have to fix their bugs or redo their work constantly and this is much more time consuming than doing it yourself the first time around. Of course this time is spent after you have spent so much time reviewing their code, and rather thoroughly, to allow their otherwise bug-ridden code in. That said, in my opinion this is just the tip of iceberg. An NNPP damages the productivity of a team on so many different levels and for someone to contribute negatively to a team they don't even have to be a slow or bad programmer: if you manage to lower the morale of a team and effectively make them less productive, even if you are a great programmer, you are still NNPP in my book.

Also I think NNPP should read Net Negative Producing Personnel or even Person. I have seen Net Negative Producing Business Analysts who drastically damage the productivity of a team due to their incorrect requirements. How about Net Negative Producing Architect, Project Manager, Manager, Tester etc? Any team member, regardless of their title, could be net negative producer. According to the [Theory of Constraints][1] "*A chain is no stronger than its weakest link*".

### Identifying an NNPP?
I have observed a few other characteristics in NNPPs. They:

 - constantly whinge about everything
 - have negative and pessimistic personalities 
 - blame everything and everyone for their low productivity
 - are very high maintenance: they ask a lot of questions to the point that makes you wonder if they can think for themselves
 - make a lot of mistakes and you have to remind them (and fix for them) the same mistakes/bugs over and over again - it feels like they never learn or learn VERY slowly. 
 - show passive aggressive behaviours 
 - lack focus and suffer from [inattentional blindness][2]

And then there are NNPPs in disguise also known as Cowboy Coders. Ward Cunningham has a good definition [here](http://c2.com/cgi/wiki?CowboyCoder) (emphasis mine):

<blockquote>
Cowboy Coders are programmers who write code according to their own rules. They may be very good at writing code, but it doesn't generally follow the standards, processes, policies, or anything else derived from the group. Cowboy Coders work well alone, or in the old-style CaveProgrammer environment, but they rarely, if ever, work well in a team. <strong>Often times, they are a burr in the saddle that keeps the team from getting positive work done</strong>.</blockquote>

... and further down he mentions:

<blockquote>CowboyCoders are identified more by their attitude than by their circumstances. CowboyCoders prefer -- nay, insist! -- to avoid standards, processes, and policies, and hate working with others.</blockquote>

Yeah, they may be great programmers in isolation but I personally want Cowboy Coders and Technical Heroes out of my team and consider them as NNPPs because although they can write high quality code fast they still slow down the team dramatically in practice. Jeffrey Snover has a beautiful example on his great post about [technical heroes](http://www.jsnover.com/blog/2012/03/18/on-heroes/):

<blockquote>As an engineering manager, I remember the first time I participated in a “life boat” drill where you have to produce a stack rank of your engineers.  Someone explained the process saying, “The task is to figure out if you had to throw out one person from a lifeboat, who it would be?  After you figure that out, then you decide who would the next one be, etc. until you have a fully ordered list.”  I chewed on that a bit and asked, “How many people are going to be left in the lifeboat?”  When they asked me why, I replied “Because if there is only one person left in the lifeboat, it would be Mark but if there was more than one person left, Mark would be the first one I’d throw out.”  Mark was a technical hero.  Able to accomplish a great deal but at a great cost to the the organization.</blockquote>

These are just some of the characteristics of an NNPP and as mentioned above regardless of how you do it, if you constantly lower your team's productivity, you are an NNPP.

#### Do not confuse low performers with NNPPs
Of course not all NNPPs have all these symptoms and more importantly not every programmer having one or more of these characteristics is an NNPP. So please do not go around your office labelling your team-mates as NNPPs just because they show some of these characteristics:

 - Some programmers are not NNPPs even though they have negative contribution. A good example of this is junior developers. You may hire a very talented junior developer and it is going to cost you a fair bit to up-skill them; but that pays dividends.
 - Some programmers also fall into the NNPP camp because they are shy or socially awkward. Try to work with them, mentor them, walk with them a few steps and let them take a few steps on their own. They are likely to learn and become better and more productive.  
 - Some programmers may be unproductive because they cannot manage their tasks or time effectively. Perhaps they are doing a lot of multitasking, and constant context switching may be the reason behind their low productivity and lack of focus. Help them with task or time management and they may become a great member in your team. In some cases in my experience it also helps to assign time-boxed tasks directly to a team member. This helps them with task and time management and over time they may learn to do it themselves.
 - Some programmers are unproductive because they are working with an NNPP! Having an NNPP in your team could make the entire team look and work like NNPPs. Deal with  the real NNPP (more on this below) so the rest of the team can fly again.

Also, as I have [ranted here](/never-judge-a-programmer-by-their-commit-history), you should never use a programmer's commit history as an indication of their productivity/skills. 

The bottom line is do not confuse every unproductive team member as an NNPPs even if they slow you down or sometimes contribute negatively to the team; but at the same time do not ignore NNPP signs. If you know someone is an NNPP the time you spend mentoring or helping them is the time a good member of the team is wasting on a bad member. So you basically end up contributing to their negative impact to the overall team productivity!

### How to deal with NNPPs
Now that we know who NNPPs are how do we deal with them?!

#### Do not hire them!
**Do not hire them**! Seriously, the best way to deal with NNPPs is to not deal with them at all. 

A while back I wrote that in my opinion [writing bad code](/bad-code) might be ok under some critical circumstances. That is, there are scenarios and situations that warrant you to (knowingly) write bad code. But **hiring a bad employee is never ok**. An NNPP does not help you ship product. They instead slows you down. So you are shipping two features a week and you think you have little budget and want to hire a new dev so you can ship more features. Wrong! Hiring a below average programmer is going to slow you down and hiring an NNPP will bring your productivity and your product down to its knees. Improve your hiring process and save yourself and your team from all this trouble and pain. 

All the successful companies I have seen and have worked for/with have had very rigorous hiring process. As the result the company is a more pleasant place to work and the staff become more productive and also stay around for a long time because they do not have any reason to leave. 

Jeff Atwood has a good post about [how to hire a good programmer](http://www.codinghorror.com/blog/2012/03/how-to-hire-a-programmer.html). It may look time consuming, expensive or even excessive but believe me that investment is well worth the result. You may think that you are small company and cannot afford that much rigor. I personally believe every team and organization can afford it and is better off with this; but if you do not agree and think that is only suitable for some "special" companies/businesses then do not go all the way there; but at least have some sort of hiring process in place that if does not get you the exceptional people at least helps you avoid the NNPP. It is not that hard.

#### Fire them!
So you have hired yourself an NNPP: congratulations. You just lost a lot of productivity in your team plus perhaps 40% of total salary you pay to the entire team (on a small team) for the time they spend maintaining and cleaning up after your new hire. Do yourself, your team and the entire organization a favor and **fire them before s/he takes you all down**. 

In some organizations firing is not quite acceptable and could cost you the morale and sense of security of the team. So you need to be careful with this. That said, I believe a bad employee is like a [broken window](/zero-tolerance-on-broken-windows) and unless you show zero tolerance you will end up with lots of them. A sad side-effect I have observed is that some good programmers or programmers with great potentials lose their motive very quickly and may even become NNPP (mostly temporarily) when working for a long time with NNPPs. 

If you think your team is not productive, do not hire a new programmer, fire the NNPP. As Gordon says:

<blockquote>Taking a poor performer off the team can often be more productive than adding a good one.</blockquote>

I have worked in a few teams of mixed experts and NNPPs and I just could not agree more with the above statement.

#### Figure them out!
So you know you have an NNPP and you do not want to or cannot fire them!! There may still be some chance to reduce (or in some cases avoid) the damage.

Some great programmers sometimes look and act like NNPPs under certain circumstances!! This in my experience happens when they do not like the task they are given or their team or their lead/manager. This is relatively easy to deal with. If they don't come to you, you should try to find out what is bothering them (in a subtle way maybe): give them a different task and if that does not work move them to different projects so they will work with a different team, team lead, manager etc. This may make them a happy person and a productive programmer again. You will salvage a good programmer in your team and the entire team will love you for this.

That trick will not work for cowboy coders! Cowboy coders are very passionate about their work but they just cannot work in teams. So if you have some work that someone could do in isolation and you want it done fast then just give it to them and get them off the team. This way you will get them to work on something that could benefit the organization while avoiding the team slow down. In fact **most NNPPs can be utilized much better in isolation** because if they cannot hide their lack of productivity behind the team's curtains they are going to pick up the slack. Also the fact that they are not part of team removes their hindrance on the team and let them fly again. 

But maybe they were not born to be a programmer and if they did not find this out this is going to be really hard for you to find out; but it may be worth a shot. Give them a different job: for example give them more testing responsibility and they may become a great QA and love you for it. Just find something else you think would suit them. 

If you cannot find them a relevant job, just keep them off coding and as far away from the team as possible. If you can find them a relevant job/place that they like and that makes them more productive then that is double win: you will get yourself a good employee and they will like what they do and will be appreciative of your support. Either way you will bring an entire team and product out of misery. 

Likewise giving more responsibility to some low performing people could bring the best out of them; but you have to be REALLY careful with this. NNPPs know they are not productive and know they cannot move forward in their career through creativity and productivity; so they welcome every single opportunity to move forward. The last thing you want to deal with is an net negative producing team leader or manager who could do very severe damage to a project. I worked on a project where a project manager took a team including a few brilliant programmers down with him, made a huge mess of the product, caused the project take three times longer and led us to a very low quality deliverable. Two of us who brought the issues to his attention faced his wrath and two brilliant (and lucky) developers who had the choice left the project. A few of us stopped caring because no matter how hard we tried or how good we were our efforts would not pay off and a lot of times we had to rework what we had already done a few times. **The more power an NNPP has the more damage they cause.**

### A word to NNPP
Honestly what I am about to say is not me being harsh on you - I am just trying to help. 

If you are an NNPP and you have always been one, then maybe this is not a job for you. Perhaps try some other profession and you may find yourself very productive and happy again. I think being an NNPP should be really hard. So do yourself, your family and your current and prospective team mates a huge favor and change your job. You better than anyone else know your passion, your strengths and your weaknesses. If you like computers then maybe try some other computer related job. Give QA or database or network administration a go and you may love it. If you are not that much passionate about computers then try some other professions. I know a female programmer who gave up programming for pharmaceutical science and every time I saw her she would tell me how she wasted five years of her life on programming and how happy she now was. She actually became very good at her second job. Passion is a great part of becoming good at something.
 
If you are usually very productive and right now find yourself in the NNPP camp then maybe ask your boss for a different task: something you will love. If it is not about your current task and about this Joe guy in the team who gives you grief, talk to Joe and sort it out. If it is about your manager try to change your department if possible or just quit and find yourself an employer/environment you will love. Martin Fowler says: *"If you can't change your organization, change your organization!"*.
 
## Conclusion
I guess any developer can more or less relate to this post: we have all worked with NNPPs and I guess you agree that it is just not fun. 

This post was about some of the things I have tried with NNPPs leading to a bit of success with some NNPPs: some of them became less of a damage and some became just a tiny bit productive. That is why I think the best way to deal with them is to not hire them or fire them; because it takes so much effort to figure an NNPP out and fix them up and I think in a lot of cases this effort just does not pay off. If we did not tolerate NNPPs through out the industry then I think they either would pick up the slack and become better or would just pick a profession they could do better.

Also I would like to add that this post is not just about programmers or even I.T. field. In my opinion net negative producers are in all industries and I think they all share the same trait and what I explained above about identifying and dealing with them could be more or less applied in any industry.

I would love to hear your thoughts and experience on this topic too. So please leave me a comment.


  [1]: http://en.wikipedia.org/wiki/Theory_of_constraints
  [2]: /inattentional-blindness