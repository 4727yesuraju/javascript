# JavaScript Data Types

## 1. 📖 Simple English Explanation

A **data type** tells us what kind of value a variable contains.

JavaScript has **8 data types**:

```text
Primitive
├── String
├── Number
├── BigInt
├── Boolean
├── Undefined
├── Null
├── Symbol
└── Object
```

The first **7 are primitive types**.
**Object** is a non-primitive type.

## 2. 🤔 Why is it Needed?

Data types help JavaScript understand **what kind of data we are working with**.

For example:

* `"Hello"` → text
* `25` → number
* `true` → true/false value
* `undefined` → value not assigned
* `null` → intentionally empty value
* `{}` → object containing data

## 3. 🌊 Flow

```text
JavaScript Value
      ↓
Identify Data Type
      ↓
Primitive or Object
      ↓
Perform Appropriate Operation
```

### Primitive vs Non-Primitive

```text
Data Types
    ↓
┌───────────────┐
│   Primitive   │
├───────────────┤
│ String        │
│ Number        │
│ BigInt        │
│ Boolean       │
│ Undefined     │
│ Null          │
│ Symbol        │
└───────────────┘

┌───────────────┐
│ Non-Primitive │
├───────────────┤
│ Object        │
└───────────────┘
```

## 4. ✍️ Syntax

```js
const name = "John";       // String
const age = 25;            // Number
const bigNumber = 123n;    // BigInt
const isActive = true;     // Boolean
let value;                 // Undefined
const empty = null;        // Null
const id = Symbol("id");   // Symbol
const user = { name: "John" }; // Object
```

## 5. 💻 Example

```js
const name = "Yesu";           // String
const age = 25;                // Number
const salary = 50000n;         // BigInt
const isDeveloper = true;      // Boolean

let city;                      // Undefined

const address = null;          // Null

const id = Symbol("userId");   // Symbol

const user = {                 // Object
  name: "Yesu",
  age: 25
};
```

You can check a value's type using `typeof`:

```js
console.log(typeof "Hello");  // "string"
console.log(typeof 25);       // "number"
console.log(typeof true);     // "boolean"
console.log(typeof undefined);// "undefined"
console.log(typeof {});       // "object"
```

> **Important:** `typeof null` returns `"object"`. This is a historical JavaScript behavior.

## 6. 🧠 Memory Trick

Remember:

> **SNB UNBS + Object**

```text
S → String
N → Number
B → BigInt
U → Undefined
N → Null
B → Boolean
S → Symbol

+ Object
```

**7 Primitive + 1 Object = 8 JavaScript Data Types**
