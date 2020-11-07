---
layout: post
title: You aren't gonna need it approach for legacy applications
date: 2013-12-15 00:01:58.000000000 +05:30
type: blog
date: 2013-12-15T00:00:00-00:00
draft: false
---
Recently I learnt about one more agile terminology. Eventhough my project is following [Classic SDLC](http://en.wikipedia.org/wiki/Waterfall_model) I am expediting agile methodolgies like [TDD](http://en.wikipedia.org/wiki/Test-driven_development) , [Kanban](http://en.wikipedia.org/wiki/Kanban_%28development%29) and few more still expediting. <br>
**Why am I doing this?**<br>
_Just to make my job interesting by myself and set myself on par with real industry_
<br>

Today I just learnt one another term which is used in [XP](http://en.wikipedia.org/wiki/Extreme_programming). The term is  **YAGNI**. I got know such a term exist from a quora [question](http://www.quora.com/Computer-Programming/Do-you-respect-the-YAGNI-principle-when-coding/answer/Kiran-Gangadharan?share=1).

Maybe I dunno the term alone but once i read about it I came to know this is very much applying in my daily job of writing code.

YAGNI stands for **You aren't gonna need it!!**. I learnt more about it from the Quora [question](http://www.quora.com/Computer-Programming/Do-you-respect-the-YAGNI-principle-when-coding/answer/Kiran-Gangadharan?share=1) and [Wikipedia](http://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it).

**So how this applies to my daily job?**

I develop for a legacy applications which has been live in production for more than seven years. In order to make my job interesting and leverage my Software development skills I try different ways/methodologies to do development.

So when developing in AGILE we focus on iterations to make users see the product with minimal working functionalities and improve them over the iterations. In that case we will be focussing only on the requirements and we won't be developing additional features or add additional codes which may be useful in future.

But currently I am unable to do this with my development work since legacy applications run across various countries with same flow. So now when I change a part of code or add a new piece of code to existing part I may have to consider not following the YAGNI principle. Since legacy applications developments usually happens(as far as I know) by tranforming the existing flow of logic from one technology(Initial old technology) to latest new technology. Few of them happens by writing from scratch which just provides the functionalities, whereas most of them follows transforming the logic into different programming language. As result of this adding new features is having great impact on exiting live code.
For example lets consider a new feature of developing a interface from legacy system to a financial system. In this case when I develop the new interface feature I have consider writing code for all the scenarios in which the existing legacy system works(eg.countrywise).Even though the interface might/won't be available in future. 
So writing such codes for legacy applications makes the development process more complex by unit testing a piece of code that won't be used when it goes live as part of this release.This has following impacts directly
*Delivery time may get delayed. <br>
*Users may not be able to see the feature on time.<br>
*Developer's focus on current deliverables shift to a more generalized solution which may not be thought during the analysis/design phase.

From management perspective they want the feature to be more generic such that write once deploy anywhere. But for applications where the logic has been merely transformed from legacy code this may not be possible.

I am facing the above issue very much in my development nowadays.....There are two solutions for my problems
*Either follow AGILE process completely where our focus completely on current release alone so developer need not think about future implementations
*Rewrite the code completely with more object oriented language such the implementations are so easy with minor tweaks.








