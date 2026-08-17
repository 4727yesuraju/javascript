# How JavaScript Works

## 1. 📖 Simple English Explanation

JavaScript code is executed by a **JavaScript engine**.

In the browser, the engine reads the JavaScript code, converts it into a form the computer can execute, and runs it.

For example, Chrome uses the **V8 JavaScript engine**.

JavaScript is **single-threaded**, which means it executes one main piece of JavaScript code at a time.

## 2. 🤔 Why is it Needed?

Understanding how JavaScript works helps us understand:

* How JavaScript executes code
* Why JavaScript is single-threaded
* How asynchronous operations work
* How JavaScript handles multiple tasks
* Why the Event Loop is important

## 3. 🌊 Flow

```text
JavaScript Code
      ↓
JavaScript Engine
      ↓
Parse Code
      ↓
Compile / Optimize
      ↓
Execute
      ↓
Call Stack
      ↓
Event Loop handles async tasks
```

For asynchronous operations:

```text
JavaScript Code
      ↓
Call Stack
      ↓
Async Operation
      ↓
Web API / Runtime
      ↓
Callback Queue
      ↓
Event Loop
      ↓
Call Stack
      ↓
Execute Callback
```

## 4. ✍️ Syntax

```js
console.log("Hello");

const a = 10;
const b = 20;

console.log(a + b);
```

## 5. 💻 Example

```js
console.log("Start");

setTimeout(() => {
  console.log("Timeout");
}, 0);

console.log("End");
```

Output:

```text
Start
End
Timeout
```

Why?

```text
console.log("Start")
      ↓
Call Stack executes it

setTimeout()
      ↓
Browser/runtime handles the timer

console.log("End")
      ↓
Call Stack executes it

Timer completes
      ↓
Callback Queue
      ↓
Event Loop
      ↓
Call Stack
      ↓
"Timeout"
```

The `setTimeout` callback does **not** execute immediately because JavaScript finishes the synchronous code first.

## 6. 🧠 Memory Trick

Remember:

**Code → Engine → Call Stack → Runtime → Queue → Event Loop → Call Stack**

Simple rule:

> **JavaScript executes synchronous code first. The Event Loop helps JavaScript handle asynchronous work.**
