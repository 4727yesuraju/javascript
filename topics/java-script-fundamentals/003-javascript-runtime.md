# JavaScript Runtime

## 1. 📖 Simple English Explanation

A **JavaScript Runtime** is the environment where JavaScript code runs.

It provides the **JavaScript Engine** and other features needed to execute JavaScript.

For example, a browser provides JavaScript with **Web APIs**, while Node.js provides APIs for server-side operations.

## 2. 🤔 Why is it Needed?

The JavaScript engine alone cannot do everything.

The runtime provides additional features such as:

* Timers
* DOM APIs in browsers
* Network requests
* File system APIs in Node.js
* Event Loop
* Callback mechanisms

So, the runtime allows JavaScript to interact with the **outside world**.

## 3. 🌊 Flow

```text
JavaScript Code
      ↓
JavaScript Runtime
      ↓
JavaScript Engine → Executes JavaScript
      ↓
Runtime APIs → Handle external/async operations
      ↓
Event Loop → Coordinates callbacks
      ↓
Call Stack → Executes callback
```

### Browser Runtime

```text
Browser Runtime
 ├── JavaScript Engine
 ├── Web APIs
 ├── Callback Queue
 └── Event Loop
```

### Node.js Runtime

```text
Node.js Runtime
 ├── V8 JavaScript Engine
 ├── Node.js APIs
 ├── libuv
 ├── Event Loop
 └── Thread Pool
```

## 4. ✍️ Syntax

> Syntax is not applicable because JavaScript Runtime is a concept.

## 5. 💻 Example

```js
console.log("Start");

setTimeout(() => {
  console.log("Timer");
}, 1000);

console.log("End");
```

The runtime handles the timer while JavaScript continues executing other code.

```text
Start
  ↓
setTimeout → Runtime handles timer
  ↓
End
  ↓
Timer completes
  ↓
Event Loop
  ↓
Callback executes
  ↓
Timer
```

## 6. 🧠 Memory Trick

Think:

> **JavaScript Engine = Brain** 🧠
> **Runtime = Complete Environment** 🌍

**Engine executes JavaScript.**
**Runtime provides everything JavaScript needs to interact with the outside world.**
