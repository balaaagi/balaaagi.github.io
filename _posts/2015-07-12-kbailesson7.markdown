---
layout: post
title: KBAI Lesson 5 -Incremental Concept Learning
date: 2015-07-12
categories: omscs

---
It's been almost a month since I watched the lecture series to cope for the classes. It's because of this concentration loss or focus on learning that I was not able code properly for Project 2 as well as my Assignment 4 got some poor grades.

The plan for today is to complete all the backlogs of lecture series and write corresponding learning blogs for the same. This will make sure that I prepare well for the final exam as well my approach towards project 3 improves my solution.



Incremental concept learning is a process in which the agent tries to learn a concept by using various cases provided to it.

### Why a concept is required?

We need concept for atleast to define a agent basic steps or variablizing the activities of the example. We should be able to generalise or specialise a concept based on our learning.

###Generalisation

Concept generalisation can be performed using heuristics. There are various types of heuristics that can be done to generalise a concept.

* Require link heuristics- link must be present to be a positive  example of the concept
* Forbid Link heuristics- link must be absent to be a positive example of the concept
* Drop link heuristics - link is not necessary to be a positive example of the concept
* Enlarge set heuristics - mutiple objects or links may fit one role in the concept
* Climb Tree heuristics - generalise over mutiple objects in the same knowledge Based
* Close Interval heuristics- Expand range of values to be a positive example of the concept


###Background knowledge

Heurisitcs can be used for building the background knowledge which will be very usefull in learning a concept. Background knowledge is like having base details about the concepts
*eg :  Base details about the shapes*

###Cognitive Connection
Incremental concept learning is similar way in which human learn from examples. But humans at time learn with only one example. Whereas an AI agent has to learn from huge no of examples at a single instance for it learn about a concept.
Case based reasoning very strong connection with human cognition.
* Problems which are identical we just retrieve those solutions
* Problems which are totally dissimilar
* Problems which are closely similar but we need to tweaking existing solutions.

Learning is important. Memory is important because we need to retrieve when needed. Reasoning is important because we need to tweak solutions when needed.
