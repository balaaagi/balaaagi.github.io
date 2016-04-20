---
layout: omscspost
title: KBAI Lesson 4 -Case Based Reasoning
date: 2015-05-31
categories: omscs
term : Summer '15
course: CS7637
---
Case Based Reasoning is like modifying the already available solutions for similar problems in memory and provide a solution to the current problem.

* If in case we don't find the exact similar case available in memory we should be able to reason the problem and adapt the solution based on the problem.

The following is how the Case Based Reasoning works

* Retrieval of cases - Retrieve a similar case from memory for the problem
* Adaption- Checking on the solution of the case problem and try to fit it into the current problem
* Evaluation - Evaluate the tweaked solution for the current problem
* Storing- If evaluation passes our criteria then the solution along with the problem case has to be stored in memory for future usage


###Assumptions of Case Based Reasoning
Following are the assumptions on case based reasoning
* Always there exists a pattern in the problems
* Similar problems have similar solutions.This may not be true in all cases

###Case Adaption using Models
We use the already available models for us to adapt the case to the existing problem.
A few examples like
* *Identifying routes from office --> restaurant. We have models for office--> doctor which is very near restaurant. Hence we adapt that model and tweak it for our problem*
* *File operations in programming. Once we have model in which file operations works in one programming language we can easily adapt it for other programming languages*

###Case Adaption using Recursive Reasoning
This method is mostly solving the problem recursively until we find the complete solution. For the given problem we may have the solution partially in our memory. We retrieve those and this is just a partial solution to the problem. Once we retrieve those we feed the remaining problem. Again similar steps occur which may have complete solution for the input or just again a partial solution. Once we have various partial solution we just combine them to arrive at a final solution.

###Case Adaption based on Rules

It is just based on the rules for given problem. If we apply the rule we may get the desired results

###Case Evaluation
In order to evaluate a case with tweaked solution from already available cases we can do either of the below
* Simulate
* Execute

Execution may not be easy in all the cases or domains. Hence simulation might be a better option before we even execute. Eg like prototyping a solution design

###Case Storage
Two Kinds of Mechanisms

* Indexing-  In this method we just store data about each case in tabular way,  so that based on that if in case some future problem comes with similar data we can use them

* Discrimination Tree-  Not a binary tree but it is like a root node having a question for which based on the answers the path differs final arrives at a  case. For adding a new case we need to follow the same tree path and add it. If in case if there exists conflicts between cases then we need to find a new root node and segregate them.

###Case Retrieval

* Tabular Index Way- We just try to compare the strings based on the stored data and retrieve results

* Discrimination Tree- We flow through the tree
and arrive at solution based on existing tree.


In general case based reasoning need not be linear. It can go through any various paths based on the results at each steps. There are possibility that few cases may not even require adaption since the retrieval may just pass the case problem.
Storing fail case may also help us in times to anticipate for new problems.
We need not store all the success cases. Only storing cases which may solve larger subset of problems will help us.

###Cognitive Connection
Case based reasoning very strong connection with human cognition.
* Problems which are identical we just retrieve those solutions
* Problems which are totally dissimilar
* Problems which are closely similar but we need to tweaking existing solutions.

Learning is important. Memory is important because we need to retrieve when needed. Reasoning is important because we need to tweak solutions when needed.
