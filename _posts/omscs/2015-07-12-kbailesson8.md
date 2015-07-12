---
layout: omscspost
title: KBAI Lesson 6 -Classification
date: 2015-07-12
categories: omscs
term : Summer '15
course: CS7637
---
Classification is one of the important topics in AI. All agents will perform this type in one way or the other.

### What is Classification?

It is like extracting a set of concepts into a sequential set of classes.

###How can it be done?

There are three major type of concept classification as below
  * Axiomatic concepts
  * Prototype concepts
  * Exemplar concepts



####Axiomatic concepts

These are the set of concepts which have proper definition or formal set of conditions. These are easily programmable via computer agents.
*Eg Definition of a circle*  

###Prototype concepts

These are like base concepts which will be overrided to its own values for other set of concepts. This is little difficult to program via computer agents
*Eg Chair Definition*

###Exemplar concepts

These are the general abstractions of the particular concepts. Very Very difficult to program via computer agents
*Eg defintion of beauty could be a painting, flower, natural scenary or beautiful girl*

###Top Down Approach

In classification a bird we use top down approach where we know that birds belongs to vertebrate and in vertrabate we have more types and birds is one among them . With this background knowledge we are able to classify the birds

###Bottom Up Approach

Bottom up approach is a method in which we try to learn the concept of the bottom tree values based on which we abstract to base root values to get the concept.


###Cognitive Connection

One typical example of cognitive connection of classification to humans is the way how doctors classify the symptoms to a disease and based on that medication is provided

Another example is how developers approach the bugs in the programs. They classify under different categories and provide fix for the bugs based on background knowledge. 




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
