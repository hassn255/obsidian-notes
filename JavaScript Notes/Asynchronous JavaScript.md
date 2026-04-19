

# How to do this

JavaScript is a single-threaded programming language. This means that the JavaScript engine has only one call stack. Therefore, it only can do one thing at a time.

When executing a **script**, the JavaScript engine executes code from top to bottom, line by line. In other words, it is synchronous.

Asynchronous means the JavaScript engine can execute other tasks while waiting for another task to be completed. For example, the JavaScript engine can:

- Request for data from a remote server.
- Display a spinner
- When the data is available, display it on the webpage.

To do this, the JavaScript engine uses an [event loop](https://www.javascripttutorial.net/javascript-event-loop/), which will be covered in the following tutorial.

## Summary

- JavaScript engine uses a call stack to manage execution contexts.
- The call stack uses the stack data structure that works based on the LIFO (last-in-first-out) principle.