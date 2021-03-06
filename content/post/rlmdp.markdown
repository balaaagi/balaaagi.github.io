---
layout: post
title: Reinforcement Learning - Markov Decision Process
date: 2016-04-13
type: omscs

date: 2016-04-13T00:00:00-00:00
draft: false
---

### Introduction

* In Supervised learning we are given `x` and `y` and we should find the `f(x)`using function approximation techniques.
* In Unsupervised learning we are give `x` and we should using clustering methods to find the `f(x)`

#### Reinforcement Learning

  In reinforcement learning we are given `x` and `z` we should find `y` and `f(x)`

  ## Markov Decision Process
  * States- Each step or states
  * Actions - Actions that can be taken in a particular state
  * Models - Transition steps in which it changes from one state to another state using particular action
  * Rewards - Rewards you get when you perform some action or when you reach a state or when you reach a state from another state using an action

  ### Properties:
  * Only Present state matter
  * Actions/States are stationery

  ### Policy
  Given a particular state a policy will suggest you a particular action to be taken
  ### Optimal Policy
  It is a policy which will help in optimize in receiving a maximum rewards.

  Hence in reinforcement learning `x` refers to state, `z` refers to rewards
  `y` refers to the actions and `f(x)` refers to the optimal policy

  ### Temporal Credit Assignment
  Identifying the action of which made us to get the rewards or for the given state we are in what was sequence of actions that was taken.

  Carefully choosing the rewards will determine the end results. 

  ## Sequence of Rewards
  * ### Infinite Horizons 
        We have ample time or no of steps to reach destination. Hence being stationery in fine.
  * ### Finite Horizons 
        Depending on the time or no of steps our actions differs
        Hence policy can be defined as the factors of both states and times
  * ### Utility of Sequences 
        Rewards we get via a sequence of states