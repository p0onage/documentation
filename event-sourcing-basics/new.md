# Overview

A lot of different terms are often thrown into the mix when discussing event sourcing that are complementary to the pattern, but not always needed. Let's begin with a basic definition.

## Event Sourcing

Event sourcing is persisting changes to application state as an ordered sequence of events. You can then calculate the current application state from replaying the history of events, instead of directly checking it.

{IMAGE}

The pattern is especially useful for distributed systems with multiple asynchronous as it helps you trace what events occurred within the application as a whole.

## CQRS

## Aggregates

## Subscriptions

## Projections

## Stream processing

## More terms to follow…
