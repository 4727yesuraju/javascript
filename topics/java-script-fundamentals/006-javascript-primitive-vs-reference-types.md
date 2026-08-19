# Primitive vs Reference Types

## 1. 📖 Simple English Explanation

JavaScript values can be understood as **Primitive** and **Reference** types.

**Primitive values** store the actual value directly.

**Reference values** store a reference to an object in memory.

Primitive types are:

```text
String, Number, BigInt, Boolean, Undefined, Null, Symbol
```

Reference types are mainly **Objects**, including arrays and functions.

## 2. 🤔 Why is it Needed?

Understanding this helps you know what happens when you **copy, change, or compare** values.

The main difference is:

> **Primitive → copied by value**
> **Reference → copied by reference**

This is very important in JavaScript interviews.

## 3. 🌊 Flow

### Primitive

```text id="a7k31p"
a = 10
 ↓
Copy value
 ↓
b = 10

a and b are independent
```

### Reference

```text id="p8s42m"
a = { name: "John" }
       ↓
   Object in Memory
       ↑
b ─────┘

a and b refer to the same object
```

## 4. ✍️ Syntax

```js id="z8xq1m"
let a = 10;
let b = a;
```

```js id="0z3v3q"
let user1 = { name: "John" };
let user2 = user1;
```

## 5. 💻 Example

### Primitive — Copy by Value

```js id="j6f4kp"
let a = 10;
let b = a;

b = 20;

console.log(a); // 10
console.log(b); // 20
```

Changing `b` does not affect `a`.

### Reference — Copy by Reference

```js id="c1q7hs"
let user1 = {
  name: "John"
};

let user2 = user1;

user2.name = "David";

console.log(user1.name); // David
console.log(user2.name); // David
```

Both variables refer to the **same object**.

### Common Reference Types

```js id="n5v2de"
const user = {
  name: "John"
};

const numbers = [1, 2, 3];

const greet = function () {
  console.log("Hello");
};
```

Objects, arrays, and functions are reference types.

## 6. 🧠 Memory Trick

Remember:

> **Primitive = Value 📦**
> **Reference = Address 🔗**

```text id="x2m8qa"
Primitive
→ Copy the value
→ Independent

Reference
→ Copy the reference
→ Same object
```
