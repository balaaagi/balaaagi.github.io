---
layout: post
title: CreditMantri Days
date: 2019-03-15 02:19
summary: Being an Engineer at FinTech
type:
date: 2019-03-15T00:00:00-00:00
draft: false
---

After a stint of almost 7+ years developing enterprise software wanted to work with startups. Having multiple offers in hand I preferred to choose a startup  in Chennai itself. The reasons are quite common
	* Challenges ahead as part of the road map
	* Experience the Software Cycle in a fast paced environment

Joined [CreditMantri](https://www.creditmantri.com/) on November 2017 as an `Engineer`. Always love to call myself as an engineer compared to the designations. Lot of questions going in the mind

	* Will I be able to survive in the startup culture after having a comfort ride with corporates?
	* Have less knowledge in the programming stack used here? How people is going to adapt me into the situation.


Even though I have no prior experience in the programming language but have good exposure to the architecture and the database used. Hence from day one started looking into the code base. 

## Making CI/CD a practice
As a first step to get into the stack introduced proper deployment strategy for the applications. Setup the infrastructure required for the [GOCD](https://www.gocd.org/). Created first versions of the production pipelines for core applications. Ensured that the new hire devops is taking control over the deployments and everything is via pipeline

## First Lines of Ruby Code
For one of the product feature which needs to built from scratch instead of using `Java` explored `Ruby`. Wrote the first version of the application using [Sinatra](http://sinatrarb.com/). Made sure there is good test coverage for the code written. 

## Gateway
It was my responsibility to rearchitect the existing application into scalable µServices. In order to that started of with the first layer a [`Gateway` ](https://microservices.io/patterns/apigateway.html). Used [Spring Boot](https://spring.io/projects/spring-boot) and Netflix's [Zuul](https://github.com/Netflix/zuul). This became the first `Java` code base for the company.

## More Java Services
As part of the rearchitecture wanted to revamp existing functionalities but due to product priorities and timelines started writing fresh functionalities as clean µService with defined scope. Made sure that tests are written.

## Containerzing the Application
Now pipelines are present and stable. But still code was present in the server. Started containerizing the java applications and ensured only images are deployed in the server. The same was setup as pre requisite for any new service

## µService Project generator
Since many new services are being born wanted to ensure all follows same project standards. Created a project generator utitlity using `maven` features and ensured any new service was strucutured in same way. This helps in logs standardizing, configuration standardizing .

## Standard Security Library
As a fintech startup had an opportunity to work with various banks and NBFCs. Developed the first version of security library that became the standard henceforth for all applications.

## Domain Specific Language
As part of various products we were in need to rule engines. Conceptualized and wrote the DSL library and used it to create a rule engine which was scalable,testable and configurable. The library was used to create many rule engine which had different types of functionalities.

## InfraStruture Cost Optimization
Revisited cloud provisioning and the way application was hosted and reachitected them to optimize monthly cost spent on infrastructure


## Infrastructure as Code
In order go to a place of reproducable infrastructure and to help in provisioning on the fly for need we need to maintain infrastructure as code. Pioneered writing terraform scripts and modules.

## Hiring Process Revamp
More services more engineers are need to maintain them. The existing hiring process was not spool proof. Revamped the process by introducing hands on way to screen candidates. This helped in filtering the candidates and made sure any engineer who is having solid hands on does not gets missed the opportunity.


The above are the major stuffs that was done during my days at CreditMantri . I was able to easily relate to the old stack and ensured that only the required components were rewritten in different stack.

It was great working with the team. 





