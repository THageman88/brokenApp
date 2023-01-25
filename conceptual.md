### Conceptual Exercise

Answer the following questions below:

- What are some ways of managing asynchronous code in JavaScript?
Use asyn and await functions to implement promises

- What is a Promise?
Promises are the foundation of asynchronous programming in modern JavaScript. A promise is an object returned by an asynchronous function, which represents the current state of the operation. At the time the promise is returned to the caller, the operation often isn't finished, but the promise object provides methods to handle the eventual success or failure of the operation. -https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Promises

- What are the differences between an async function and a regular function?
The async function declaration declares an async function where the await keyword is permitted within the function body
A regular function 

- What is the difference between Node.js and Express.js?
Node.js is an open source and cross-platform runtime environment for executing JavaScript code outside of a browser
Express is a small framework that sits on top of Node.js web server functionality to simplify its APIs and add helpful new features

- What is the error-first callback pattern?
Error-First Callback in Node.js is a function which either returns an error object or any successful data returned by the function

- What is middleware?
Middleware is the layer that exists between the application components, tools, and devices. With middleware, you can simplify connectivity between the components. Node.JS middleware plays a prime role in the request-response lifecycle of Node.JS execution.

- What does the `next` function do?
Skips the current middleware function and passes controll to the next route

- What are some issues with the following code? (consider all aspects: performance, structure, naming, etc)

```js
async function getUsers() {
  const elie = await $.getJSON('https://api.github.com/users/elie');
  const joel = await $.getJSON('https://api.github.com/users/joelburton');
  const matt = await $.getJSON('https://api.github.com/users/mmmaaatttttt');

  return [elie, matt, joel];
}
```
you could create a variable called name and use that with a variable called url to shorten the calls
You can call the next function so you are able to continue while waiting on your promises,
