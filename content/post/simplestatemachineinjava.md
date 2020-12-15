---
title: "Simple State Machine In Java"
date: 2020-10-06T18:21:37+05:30
summary: "Implementing State Machines in Java"
draft: false
categories : [ "java"]
---

# Simple State Machine in Java


## What is a State Machine ?

[Wikipedia defines a finite-state machine (FSM)](https://en.wikipedia.org/wiki/Finite-state_machine) as:
> an abstract machine that can be in exactly one of a finite number of states at any given time. 
> The FSM can change from one state to another in response to some external inputs; the change from one state to another is called a transition. 
> An FSM is defined by a list of its states, its initial state, and the conditions for each transition.


It is way to program a model so that it is at one particular state at any moment. 

The world is filled with state machines which we can see anywhere in our daily usage. Below are few

* Road Traffic Signale Red -> Yellow -> Green
* Coffee Vending Machine
* E-commerce Portal Ordering
* Online Trip Booking
* Many Cron Jobs

## Implementing State Machines In Java

There are many ways which we can implement state machines. In Java world itself we have many libraries using which we can model these states
* [Spring State Machine](https://projects.spring.io/spring-statemachine/)
* [Squirrel](https://github.com/hekailiang/squirrel)

We can also implement them using a standard `State Design pattern` [example] https://www.journaldev.com/1751/state-design-pattern-java)

What if we don't want to add any external dependencies?
What if we want to have simple state machine and control it via our own logic?

## State Machines Using Enums in Java

Many of us would have used Uber or Ola at-least once. Lets try implementing the trip booking state machine using Java Enums

What are the ideal states in trip booking?
* Trip Booked
* Driver Assigned
* Driver Reached
* Trip Started
* Trip Ended

![](/images/tripstatemachine.png)

### Simple Implementation

```java

public enum TripStates {
    TRIPCREATED,
    DRIVERASSSIGNED,
    DRIVERREACHED,
    TRIPSTARTED,
    TRIPENDED;

}

```

The above enum can be used across our application for maintaining the state of the trip. Even in database this can be used by using the string value of the enum. Example `TripStates.TRIPCREATED.name()`



Now we have implemented the state machine but how to ensure proper state transition happens. One simple way is to include a function within the enum and check it across whenever we are trying to change the state of a trip

```java
public boolean canChangeTripState(TripStates fromState, TripStates toState){
        return fromState.ordinal()<toState.ordinal();
}

```


The above function needs to be called wherever state changes needs to happen. This helps in moving states in forward manner.
But there is problem with this. We will be able to move a trip from trip created to trip started. The above implementation might not solve the real constraint we would like to introduce like a trip cannot be marked as started without marking as reached.

How can we achieve this with just enum?

Java Enums can have additional fields to it. We can leverage that to solve this.


```java
public enum TripStates {
    TRIPCREATED(Arrays.asList(new TripStates[]{})),
    DRIVERASSSIGNED(Arrays.asList(new TripStates[]{TripStates.TRIPCREATED})),
    DRIVERREACHED(Arrays.asList(new TripStates[]{TripStates.DRIVERASSSIGNED})),
    TRIPSTARTED(Arrays.asList(new TripStates[]{TripStates.DRIVERREACHED})),
    TRIPENDED(Arrays.asList(new TripStates[]{TripStates.TRIPSTARTED}));


    private List<TripStates> validFromStates = new LinkedList<TripStates>();


    TripStates(List<TripStates> validFromStates) {
        this.validFromStates = validFromStates;
    }

    public boolean canChangeTripState(TripStates fromState, TripStates toState) {
        return toState.validFromStates.contains(fromState);
    }
}
```

If you look we are maintaining `validFromStates` in order easily expand this to other cases where a trip can ended even from different states. Example: CustomerNotReachable etc..


The above is a simple implementation that can be used. But if we wanted to have more logic within this state transitions we can still leverage but we need to hook the above model with other design patterns.