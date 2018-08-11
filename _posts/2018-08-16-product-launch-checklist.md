---
layout: post
title: "Product launch checklist"
description: "This is a checklist for everything you need to consider for launching a new product"
date: "2018-08-16"
tags: ["Product"]
---
Earlier in my career, I saw product launch through one lens: developing the software. This was partly due to my singular focus on software development and partly because that's what every company I worked for and with did. In the past few years, I've been involved in end to end delivery of several products, from idea all the way to release and market fit.

This list is based on my experience. I'm keen to hear what other consider as part of a product launch.

### User Experience
 - Before doing anything else, identify and validate the problem you're working on. [Design Thinking](https://www.ideou.com/pages/design-thinking) is your friend here.
 - Perform user/usability testing, as you start creating prototypes and develop features. I've had good experience with [User Testing](https://www.usertesting.com/services). A few things to consider for usability testing:
   - How and where do you find users?
   - Prepare the usability scripts and scenarios
   - Arrange and run interviews

### Product Management
 - Use a sound product market fit process and strategy. I am a bit fan of [Lean Startup](http://theleanstartup.com/).
 - Perform a competitor analysis to see what others are doing.
 - Develop personas for early adopters.
 - Identify early adopters.
 - Are you doing soft launch or big bang release? Do soft launch whenever possible.
 - Create and maintain a product roadmap. Refine the roadmap based on market analysis as well as the feedback from usability testing and early adopters.
 - Do you publish your roadmap? How far into the future? Don't commit to features in the far future. Your roadmap will change by the time you get there.
 - How do you gather feedback from your users? How do you prioritise their feedback along new feature development?
 - What needs to be in place before you release the product to early adopters? What needs to be in place before you open the flood gates?

### Marketing
 - Find a name! Sounds kinda funny; but a lot of people fail at this. Brain storm around possible names, pick a few that you like, google them to make sure they don't point to existing products and services and are sane keywords; e.g. don't name your product `go`.
 - Buy your domain and consider buying a few other top layer domain names for your domain; e.g. `.com`, `.com.au`, `.net`, `.io`.
 - Define a tagline for the product.
 - Define a pricing structure and strategy. Test your pricing structure with your early adopters. Do you provide a different pricing for your early adopters?
 - Think about marketing. Do you need a landing page? Who's going to write the copy? Who's going to design the landing page? Who’s going to do SEO?
 - If you don't have this already, define a brand identity: colour palettes, icons (for the landing page and the app), style guides etc.
 - Consider a launch plan. Are there magazines, blogs or publications you want to target to promote the launch of your product?
 - Do you need a social media presence? If yes, you need to start thinking about the social media persona you want to embody. Also if twitter, you need to start locking user accounts before they disappear. Who’s going to be the social media person?

### Security
 - Consider creating a responsible disclosure policy/guideline. Checkout [Tesla's](https://www.tesla.com/about/security) for inspiration.
 - Consider bug bounty programs; e.g. [bugcrowd](https://www.bugcrowd.com/bug-bounty-list/).
 - Create a data retention and destruction policy
 - Create a data breach response policy
 - Consider creating a BCP and DR policy
 - Consider performing penetration testing. If you're doing it, do good research and find reputable pen testers. Do you want to do blackbox, greybox or whitebox testing? How often would you redo the test? Does the vendor allow retest if they find vulnerabilities?
 - What kind of data would you be storing - PII, PCI, PHI?
 - What sort of regulations do you need to comply with - APP, GDPR, IRAP, NEHTA etc?
 - Do you have data sovereignty requirements?
 - Do you have a security monitoring and testing system in place?

### Legal bits
 - Create privacy agreements for your users
 - Create license agreement for your users
 - Do you need confidentiality agreement for external user testing?

### Support
 - Who’s going to provide application support for end users? And how - over the phone, in-app chat, Facebook, Twitter etc?
 - How will you communicate changes and new features to your users?
 - Do you need to develop help, documentation or FAQ for the product? Try to aim for a product that's so user friendly it doesn't need a lot of support or training.
 - Do you have a CRM? Does it fit this product?
 - How do you train your support staff with upcoming features?
 - Is your product used globally? If yes, (how) will you provide round the clock support?

### Technical
 - Do you have a logging and monitoring system?
 - Do you have health dashboards setup?
 - Write automated tests and build up your automated regression suite as you go.
 - Go at a sustainable pace. Are you writing maintainable code?
 - Can do you zero downtime release? This is much more critical if you are working on a globally used product with no "after hours".
 - Does this system need to integrate into other systems? What's the impact on other systems? Can they cope with the demands of this new product? Can this product work within those constrains? Think about chatty transactions, blocking requests, eventual consistency, security requirements, reporting requirements, human interactions etc
 - Don't leave reporting til the end. Work through reports as you're building the product.
