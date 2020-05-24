---
layout: post
title: Working for Unicorn
date: 2020-01-15 08:58
summary: Being an Engineer at Unicorn
categories:
---

After a short stint at [Creditmantri](http://blog.balaaagi.in/2019/03/15/creditmantridays/) opportunities knocked me to work for [Zomato](https://zomato.com).
I was always eager to work on scaling things and the scale at which Zomato operates is what excited me to join them. Was hired as lead engineer for their newly formed Logisitics Engineering division based out of Bengaluru. The logisitics engineering team was so young an energetic. It was after the [acquisition](https://www.zomato.com/blog/introducing-the-zomato-runnr) of that online delivery was seen as major business for Zomato. I was eager to work with folks who have built the Runnr from scractch.

* ### New City
Bengaluru has been always the tech hub of India. Have travelled from Chennai for various hackathons and meetups since it was so lively city in tech. All through my life was a Chennai guy, moving to Bengaluru had mixed feelings. Going to miss Chennai and its own flavours a lot. Initially I moved to with family moving in after few month of me settling in. 

* ### Initial Days
Similar to CreditMantri the tech stack is all new even though have got some exposure but never worked on production code base at bigger scale. It was purely `Rails` based application that was present. Lot of plans where there to revamp these into smalled microservices. There were few components running in `Java`.
Since have got some experience working in `Java` within a week of joining started contributing to rolling out features in `Java` codebase which as basically a decisioning engine used during order flow which is a tier one service.

* ### Interviewing Days 
Since we were ramping up the team members got the opportunity to be part of the panels to scale up the team. Already process was clean so it was just more of meeting new people and understanding their pros and checking for their skill fit. Lot of time was spent in interviews on avg used to spend closed to 6 hours/week on interviews alone. It continued till my last week of work but only number of hours just gradually reduced.


* ### Unit Tests
Even though have been practicising and trying to have good unit test coverage in previous stints have not come across a code with so much unit tests. May be it was  `ruby` that made it possible. Was really impressed on the way that unit tests were given so much importance which I always love too. We had scenarios when deployments were just blocked because of a single unit tests were failing. You can't allow any code to break systems at this scale. 

* ### Serverless 
One of key pains of running at this scale is maintaining the infra components. So for one of the key components which was planned designed and implemented using serverless pattern. Desigining and implementing this was so great because was easily able to reap of the benefits of this design when used at scale.

* ### Features with Impact
Lead lot of feature implementations to unblock operational issues that has resulted in huge cost savings to the company and increase the driver utilization to a great extent. 


* ### Optimzing for ms
As said earlier decisioning engine is one of the core tier one service used in the order flow. It used to have 5-10 API hits for each order for driver. In addition to that it was used in lot of offline computations too.
During peak hours (lunch/dinner) this service used to block the performance because of which we need to provision with more infra for them. Myself along with [Prakhar](https://www.prakhar.xyz/) took at as a goal to make it so optimized.It was so fun an crazy when you are playing with JVM params to optimize a service which was at response time ~110ms to even more. Atlast we made it to be  at ~ 17ms. This was so much relief an proud moment when you do this for a service which is a key service in order flow. It helped in optimizing the infra to a great extend for this service which saved huge cost to the company.

* ### Scale Scale Scale
Every line of code we wrote scale was the first thing that we thought about. It was crazy different set of experience for me. It was also because of this that allowed me to explored lot of tools and gain experience in them. Got to see real impact of small features at bigger scale. 

* ### Containerization Journey
Even though we were operating at scale containerization journey was about to kick off. The new micro service that I was building even though did not impact the order flow ensured that it was launched in production in a proper containerzed way. I would proudly say this was the first service to begin the containerization journey atleast in the logistics engineering team.

* ### New Languages & Frameworks
The huge codebase in Ruby helped me to explore rails and helped me to understand lot of implicit design considerations in Ruby. Helped in building the Version One of a new key service in GoLang. We did not use any frameworks everything was implemented using the default implementations available within the language.

* ### Data Driven Decisions
Any new line of code we wrote or optimization we did was everything was driven via a data point. Which at-least have not experienced in the past. It was so great to see the impact of whatever we do on daily basis contributing to the companies growth and impacting millions at scale. 

-----------------------

Even though the ride was short proud of the impacts that I have made during my short tenure. Lot of learnings when systems operate at huge scale. Really will be helpful for lifetime. Due to various conflicting reasons had to take a decision to quit the journey. All the people that I have worked with during my tenure there were wonderful learnt something or other from each one of them. 

  


