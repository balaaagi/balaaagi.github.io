---
layout: post
title: KBAI Lesson 3 -Production Systems and Chunking
date: 2015-05-30
categories: omscs

---
I was planning to complete the lecture by Thursday  itself along with learning  posts. But was working on Android stuffs for the Coursera Course which made me to do it today.

This lesson will be providing the details on a how a production systems of cognitive agents will be and how Chunking works.

###Cognitive Architecture
The lesson give a nice definition of Cognitive architecture by introducing a simple definition of Cognitive agent.

*Cognitive agents are agents which is like a function which maps characteristic functions to actions*

Basically it a perception which is like having a action for everything.

###Levels of Cognitive architecture

Cognitive architecture can be at various levels like below

* Hardware/Implementations Levels
* Algorithm or model levels
* Task/Knowledge levels

For IBM watson these are how these levels can be interpreted

* A working Personal computer- Hardware
* Selection and decision making- Algorithm
* Answering to input clue - Knowledge

###Assumptions of Cognitive Architecture

* Should have a goal- take actions based on goal
* Live in rich and dynamic environment
* Huge Knowledge
* Symbols and Abstractions
* Flexible and behavious is dependant on environment
* They keep on learning from their experience

    `Architecture + Content= Behaviour`

###Architecture for Production Systems
Deliberation which consists of reasoning, learning and memory.
SOAR - does this part in production systems
It has long term memory and working memory
It interact with memory in three ways
* Procedural- How to do certain things like steps
* Semantic- Generalization in form of concepts and models
* Episodic- Based on events(What had u for dinner?)

###Pitcher on selectoin of next steps
Based on the available data or content in memory for the event with a particular goal .
Contents resides in working memory
Other steps remain in long term memory
Pitcher applies procedural steps and decide on the next steps based on the goal in content
If the content changes it take according steps. If in case the system does not able to decide between two results from procedural it move to Episodic where it has particular set of memory result decision based on that.


###Chunking
Chunking is to find a rule that will break the imparse. Then SOAR searches episodic memory and find a rule. Reasoning, learning and memory are closely connected in cognitive systems.

###Cognitive Connection
SOAR architecure resembles how human solve problem for algebra and analytics. SOAR working memory is like human short term memory. Inspite of this we can't conclude that we have a solid architecture on human cognition
