# Overview

A lot of different terms are often thrown into the mix when discussing event sourcing that are complementary to the pattern, but not always needed. Let's begin with a definition.

## Event Sourcing

Event sourcing is persisting changes to application state as an ordered sequence of events over time. You can then calculate the current application state from replaying the history of events, instead of directly checking it.

The pattern is especially useful for distributed systems with multiple concurrent services as it helps you trace what events occurred within the application as a whole.

Event Sourcing removes the question of how an application got to a certain state. It lets you fully test input and output state by defining a sequence of events and what events you expect after a state change.

{IMAGE}

## CQRS

## Aggregates

## Subscriptions

## Projections

## Stream processing

## More terms to follow…
