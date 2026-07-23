# Event Loop in Node.js

---

# What is the Event Loop?

The Event Loop is the core mechanism that allows Node.js to perform non-blocking, asynchronous operations using a single thread.

It continuously checks:

- Call Stack
- Callback Queue
- Event Queue

and executes tasks in the correct order.

---

# Why is the Event Loop Needed?

Imagine a restaurant.

One waiter serves multiple tables.

Instead of waiting for one customer's food to cook, the waiter takes another customer's order.

This makes the restaurant efficient.

Node.js works in the same way.

---

# Components

```

                Event Loop

                     |

      ------------------------------

      |             |             |

 Call Stack    Callback Queue    Web APIs

```

---

# Call Stack

Stores functions currently being executed.

Example

```javascript
function first() {
    second();
}

function second() {
    console.log("Hello");
}

first();
```

Execution

```
first()

↓

second()

↓

console.log()

↓

Finished
```

---

# Callback Queue

Stores completed asynchronous callbacks.

Example

```javascript
setTimeout(() => {
    console.log("Done");
},1000);
```

After 1 second

↓

Moves into Callback Queue

↓

Event Loop

↓

Call Stack

↓

Executed

---

# Example

```javascript
console.log("Start");

setTimeout(() => {
    console.log("Timer");
},0);

console.log("End");
```

Output

```
Start

End

Timer
```

Although timeout is zero,

JavaScript finishes the current stack before executing callbacks.

---

# Event Loop Steps

1.

Execute synchronous code.

↓

2.

Move async callback to queue.

↓

3.

Check Call Stack.

↓

4.

If empty,

move callback to stack.

↓

5.

Execute callback.

---

# Why Node.js is Fast?

Node.js

✔ Single Thread

✔ Non Blocking

✔ Event Driven

✔ Event Loop

This combination allows handling thousands of requests efficiently.

---

# Real-Time Example

Restaurant

```
Customer 1

↓

Order Food

↓

Cooking Starts

↓

Waiter Serves Customer 2

↓

Customer 3

↓

Customer 4

↓

Food Ready

↓

Serve Customer 1
```

---

# Interview Questions

## What is Event Loop?

The Event Loop allows Node.js to execute asynchronous operations without blocking the main thread.

---

## Why is Node.js called Single Threaded?

JavaScript execution happens on a single thread, while asynchronous operations are delegated to system APIs.

---

## Why does setTimeout(fn,0) execute later?

Because callbacks execute only after the Call Stack becomes empty.

---

# Quick Revision

Call Stack

↓

Web APIs

↓

Callback Queue

↓

Event Loop

↓

Execution