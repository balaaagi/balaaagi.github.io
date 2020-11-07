---
layout: post
title: KBAI Lesson 1 - Generate and Test method
date: 2015-05-25
type: omscs

date: 2015-05-25T00:00:00-00:00
draft: false
---

The lectures are organised around the seven topics of AI

<img src="https://cloud.githubusercontent.com/assets/2221784/7844461/1b9d5ac4-04ce-11e5-9332-37d84f331a53.png" width="500" height="400" />

The initial set of lectures were based on covering the fundamentals. The first topic in fundamentals is Semantic Networks - a way of knowledge representation,  which I explained in my previous blog post.

The next topic is Generate and Test method. This method is way of problem solving in which we will be generate potential solutions for the problem and test those solutions to validate the results.

The professor was trying to explain what is a smart generator by giving a simple explaination. If we have complete knowledge about the world then we will be able to get <b>the solution <b> which will be always correct and optimum.We also don't need to test the solution.

On the other hand professor try to convey the other end which smart testers. Here we may not have proper knowledge of the world hence always our solution might be wrong. In this case the solutions might be just potential solutions which need a tester to validate.

##Prisoners and Guards problem
These type of problem solving was then used in solving [Prisoners and Guards problems ](https://www.youtube.com/watch?v=HcEEC4oQ6o0).

Here the first we will be generating all the potential next steps solution. Then the tester will validate and remove the not valid ones.
Possibilities that the generator and tester can both be dumb.

Since generator is dumb it will generate not valid states as potential solutions.Since tester is also dumb it will just remove the not valid states alone.But if we have a smart testers there are possibilities that the tester will be able to dismiss the identical states similar to previous states.Similarly it can happen for the smart generators too.

##Raven's Problems using Generate & Test
Using general generate and test method if we try to solve Raven's problem it may be possible for n number of possible solutions since abstraction of details matters.
In thoses scenarios our knowledge representation comes into picture. We can use Semantic Networks for this case to represent our problem.

`Knowlege Representation + Problem Solving Method - Solves the problem.`

So in order to use generate and test along semantic network representation for Raven's problem 2X2 below can be the steps

* Using representation from A--> B try a transformation from C-->D
* Use the representation of D as potential solution
* Test it i.e compare it against the given options representations
* The one that closely matches is the solution

The other way is compare the semantic network representation comparision as below
* Choose one options at time. Generate the transformation representation from C-->D
* Test it against the transformation representation from A--> B
* Find out which one is closest transformatin from A-->B


##Cognitve Connection
Humans always generate a potential solution first for any problem and then start testing it.
