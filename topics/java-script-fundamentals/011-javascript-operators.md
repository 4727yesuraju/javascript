# JavaScript Operators

## 1. 📖 Simple English Explanation

**Operators** are symbols or keywords used to perform operations on values.

For example:

```js id="x5c8zn"
10 + 5
```

Here, `+` is an operator that performs addition.

JavaScript has several types of operators:

```text id="f7y2qm"
Arithmetic
Assignment
Comparison
Logical
Increment / Decrement
Ternary
Nullish Coalescing
Optional Chaining
Bitwise
```

## 2. 🤔 Why is it Needed?

Operators are needed to:

* Perform calculations
* Compare values
* Assign values
* Combine conditions
* Increase or decrease values
* Make decisions
* Safely access data

## 3. 🌊 Flow

```text id="k2m8qx"
Values
  ↓
Operator
  ↓
Operation
  ↓
Result
```

Example:

```text id="v9q4ws"
10 + 5
 ↓
+
 ↓
15
```

## 4. ✍️ Syntax

### Arithmetic

```js id="q6x2pa"
a + b
a - b
a * b
a / b
a % b
a ** b
```

### Assignment

```js id="z8m3kr"
a = 10
a += 5
a -= 5
a *= 5
a /= 5
```

### Comparison

```js id="p4v7nd"
a == b
a === b
a != b
a !== b
a > b
a < b
a >= b
a <= b
```

### Logical

```js id="n5c8xs"
a && b
a || b
!a
```

### Increment / Decrement

```js id="w2r6hj"
a++
a--
++a
--a
```

### Ternary

```js id="e7k3qm"
condition ? valueIfTrue : valueIfFalse
```

### Nullish Coalescing

```js id="u4p9cs"
value ?? defaultValue
```

### Optional Chaining

```js id="r6n2vd"
object?.property
```

## 5. 💻 Example

```js id="b8q4mt"
const a = 10;
const b = 5;

// Arithmetic
console.log(a + b); // 15

// Comparison
console.log(a > b); // true

// Logical
console.log(a > 5 && b < 10); // true

// Assignment
let x = 10;
x += 5;
console.log(x); // 15

// Ternary
const result = a > b ? "A is greater" : "B is greater";
console.log(result); // A is greater

// Nullish Coalescing
const name = null;
console.log(name ?? "Guest"); // Guest
```

## 6. 🧠 Memory Trick

Remember:

> **A A C L I T N O**

```text id="m8x2pv"
A → Arithmetic
A → Assignment
C → Comparison
L → Logical
I → Increment / Decrement
T → Ternary
N → Nullish Coalescing
O → Optional Chaining
```

Think:

> **Calculate → Assign → Compare → Combine → Change → Decide → Default → Safely Access**
