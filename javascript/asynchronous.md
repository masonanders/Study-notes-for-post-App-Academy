# Asynchronous vs Synchronousity

## Synchronous

A synchronous language interprets and runs code one line at a time. A line cannot be executed before all other lines above it have been.

An analogy could be waiting in a line to order an ice cream. You can not start your order until everybody else in front of you has completed their order and received their ice cream.

## Asynchronous

An asynchronous language can interpret and schedule events to happen in the future. An expression can be read and put in a queue while the script continues on with it's executions.

An analogy could be a sit-down restaurant. You do not have to wait for others to sit, order, and finish eating before you can start your dining experience. The wait staff visits each table and continues on with a process only when that table is ready.

---

It is important to note that an asynchronous doesn't mean that two things are happening at once (multi-threaded). It only means that the language can switch between processes if they have an event scheduled for a future time. Kind of like a singly staffed restaurant.

JavaScript is a singly-threaded, asynchronous language.

Resources: https://www.pluralsight.com/guides/introduction-to-asynchronous-javascript