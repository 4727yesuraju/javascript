# JavaScript Variables — `var`, `let`, `const`

## 1. 📖 Simple English Explanation

A **variable** is a named container used to store data.

JavaScript provides three keywords to declare variables:

* `var` → Function-scoped
* `let` → Block-scoped
* `const` → Block-scoped and cannot be reassigned

In modern JavaScript, prefer **`const` by default** and use **`let`** when the value needs to change.

## 2. 🤔 Why is it Needed?

Variables are needed to:

* Store data
* Reuse values
* Change values when required
* Make code easier to read and maintain

Example:

```js
const name = "John";
let age = 25;
```

Here, `name` and `age` store values that we can use later.

## 3. 🌊 Flow

```text
Declare Variable
      ↓
Store Value
      ↓
Use Value
      ↓
(Optional) Change Value
```

### Scope

```text
var   → Function Scope
let   → Block Scope
const → Block Scope
```

## 4. ✍️ Syntax

```js
var name = "John";

let age = 25;

const country = "India";
```

Changing values:

```js
let age = 25;
age = 26;        // ✅ Allowed

const country = "India";
country = "USA"; // ❌ Error
```

## 5. 💻 Example

```js
function example() {
  var a = 10;

  if (true) {
    let b = 20;
    const c = 30;

    console.log(a); // 10
    console.log(b); // 20
    console.log(c); // 30
  }

  console.log(a); // 10
  console.log(b); // ❌ Error
  console.log(c); // ❌ Error
}
```

`var` is accessible throughout the function, while `let` and `const` are limited to the block `{ }` where they are declared.

## 6. 🧠 Memory Trick

Remember:

> **var = Function**
> **let = Change**
> **const = Constant reference**

Best practice:

> **`const` first → `let` when needed → avoid `var` in modern JavaScript.**
