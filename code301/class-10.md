# The Call Stack - [MDN](https://developer.mozilla.org/en-US/docs/Glossary/Call_stack) [Charles Freeborn](https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/)

The call stack is how an interpreter keeps track of functions in a script, using the last in, first out principle. Tracking what functions are on the page and adding it to the call stack and run when their invocations are reached. An error(stack overflow) occcur when the stack runs out of space assigned to it.
The call stack is synchronous so it executes functions in the order that ther are addded to the list in a singular fashion. Each function occupies temporary memory and the stack is cleard after the lsat function is run.

## JavaScript Error Messages [Diogo Spinola](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c)

Error handling (debugging) is as ubiquitous as reading and writing code to  software developers, hence, being able to read and debug error messages is a very useful skill that gets better the more you use it.
It is good practice to remove all your debugging tools from the code before a commit/push.
