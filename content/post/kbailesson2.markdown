---
layout: post
title: KBAI Lesson 2 -Mean end Analysis, Problem Reduction
date: 2015-05-27
type: omscs

date: 2015-05-27T00:00:00-00:00
draft: false
---
I was planning to complete the lecture by Monday itself along with learning  posts.
But was working on the ROFL backend service tweaking and Tuesday was completely unwell
due to which I was unable to complete the stuffs on time.

I know time for assignment one has crossed and I must for sure submit assignment two.
Also peer feedback is open for assignment one. Which also i should complete at the earliest. But I wanted to start peer feedback once
I complete the week 1 lectures so that I will be able to learn and understand the peer assignment well for peer feedback.

##What is Mean-End Analysis?

Mean end analysis is way of problem solving in which we solve problem by a path or comparing states with end state.
*   We need to find the differences each possible state with the end state.
*  We should choose the one which is having less mean average compared to
previous state.
* The mean average differences should be progressively decreasing.


The problem we are trying to solve here is moving blocks on a table.
We have some pre conditions also we have the end state on how the blocks are arranged.

###Few insights on this method of problem solving
 * Not always may end up in proper solution.
 * Very costly way to solve problems
 * Like generate and test method these are used for more general problems sets.
 * Blocks problems may not be able to solve via this method many other AI problems can be solved via this method.

##Problem Reduction
* Reducing a bigger problem into smaller set of problems
* Finding solutions for the smaller problems will be leading us to the bigger problem solution
* Universal problems are solved using this method. Not high guarantee of success.

The problem we are trying to solve is blocks problems. Here we start with the place where the Means and analysis fails and arrive at a end state of smaller solution and try to solve to arrive at original solution

##Means and Analysis for Raven's Problems
In order to solve Raven's problem via Means and Analysis method we have to do following

* Find the states which are inbetween A-->B transformation.
* Once found we need to try to replicate the same set of states transformation for C. Lot of possibilities may occur.
* On final arrival of various potential solution we have to compare with answer options to find the solution
* Here we are using semantic representation for each state, generate test method for validating final results and problem reduction as finding states of A-->B, apply the states on C, validate test against all options provided.

###Some insights
* Representation seems to common for all methods we are trying to use
* Combination of various problem solving method can be used for solving a particular problem

##Cognitive Connection
* Means and Analysis, Problem reduction and generate and test are weak methods because they use very little of knowlege.
* When humans work on domains which they are very much knowledgable then they use strong problem solving methods.
* When humans work on domains which they don't have much knowledge then they use these weak methods for problem solving.
