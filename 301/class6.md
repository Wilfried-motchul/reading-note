# Node , Express and APIs

> What Is Node and When Should I Use It?

There are plenty of definitions to be found online. Let’s take a look at a couple of the more popular ones. This is what the project’s home page has to say:

Node.js® is a JavaScript runtime built on Chrome’s V8 JavaScript engine.

And this is what Stack Overflow has to offer:

Node.js is an event-based, non-blocking, asynchronous I/O runtime that uses Google’s V8 JavaScript engine and libuv library.

Hmmm, “event-based”, “non-blocking”, “asynchronous I/O” — that’s quite a lot to digest in one go. So let’s approach this from a different angle and begin by focusing on the other detail that both descriptions mention — the V8 JavaScript engine.

* How Do I Install Node.js?
In this next section, we’ll install Node and write a couple of simple programs. We’ll also look at npm, a package manager that comes bundled with Node.

* Node.js Has Excellent Support for Modern JavaScript
As can be seen on this compatibility table, Node has excellent support for ECMAScript 2015 (ES6) and beyond. As you’re only targeting one runtime (a specific version of the V8 engine), this means that you can write your JavaScript using the latest and most modern syntax. It also means that you don’t generally have to worry about compatibility issues — as you would if you were writing JavaScript that would run in different browsers.

To illustrate the point, here’s a second program that makes use of several modern JavaScript features, such as tagged template literals, object destructuring and Array.prototype.flatMap():

```
function upcase(strings, ...values) {
  return values.map(name => name[0].toUpperCase() + name.slice(1))
    .join(' ') + strings[2];
}

const person = {
  first: 'brendan',
  last: 'eich',
  age: 56,
  position: 'CEO of Brave Software',
};

const { first, last } = person;
const emoticon = [ ['┌', '('], ['˘', '⌣'], ['˘', ')', 'ʃ'] ];

console.log(
  upcase`${first} ${last} is the creator of JavaScript! ` + emoticon.flat().join('')
);
```
