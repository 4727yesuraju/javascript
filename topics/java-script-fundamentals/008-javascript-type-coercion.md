# Type Coercion

## 1. 📖 Simple English Explanation

**Type Coercion** means JavaScript **automatically converts one data type into another** when performing an operation.

It is a type of **implicit type conversion**.

For example:

```js
"5" + 2
```

JavaScript converts `2` into `"2"` and produces:

```text
"52"
```

## 2. 🤔 Why is it Needed?

JavaScript is dynamically typed, so different data types can be used together.

Type coercion allows JavaScript to decide how to perform an operation when different types are involved.

It is important to understand because it can sometimes produce **unexpected results**.

## 3. 🌊 Flow

### With `+`

```text
"5" + 2
   ↓
2 → "2"
   ↓
"5" + "2"
   ↓
"52"
```

### With `-`

```text
"5" - 2
   ↓
"5" → 5
   ↓
5 - 2
   ↓
3
```

### With Comparison

```text
"5" == 5
   ↓
JavaScript converts types
   ↓
5 == 5
   ↓
true
```

## 4. ✍️ Syntax

Type coercion does not have special syntax.

It happens automatically:

```js
"5" + 2;
"5" - 2;
"5" == 5;
```

## 5. 💻 Example

### String + Number

```js
console.log("10" + 5);
// "105"
```

`+` with a string performs **string concatenation**.

### String - Number

```js
console.log("10" - 5);
// 5
```

`-` requires numbers, so JavaScript converts `"10"` into `10`.

### Boolean + Number

```js
console.log(true + 1);
// 2
```

JavaScript converts:

```text
true → 1
false → 0
```

### Loose Equality

```js
console.log("10" == 10);
// true
```

`==` allows type coercion.

But:

```js
console.log("10" === 10);
// false
```

`===` checks **value and type** without performing this kind of coercion.

## 6. 🧠 Memory Trick

Remember:

> **Coercion = JavaScript Converts Automatically 🤖**

Quick rule:

```text
+  → String may win
-  → Number
*  → Number
/  → Number

==  → Allows type coercion
=== → No type coercion
```
