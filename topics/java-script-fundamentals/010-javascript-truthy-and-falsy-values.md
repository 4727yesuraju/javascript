# Truthy and Falsy Values

## 1. 📖 Simple English Explanation

In JavaScript, every value can be treated as either **truthy** or **falsy** when used in a condition.

* **Truthy** → behaves like `true`
* **Falsy** → behaves like `false`

Falsy values are:

```text
false
0
-0
0n
""
null
undefined
NaN
```

**Everything else is truthy**, including:

```js
"0"
"false"
[]
{}
```

## 2. 🤔 Why is it Needed?

Truthy and falsy values are useful when writing conditions.

They allow us to check whether a value exists or has a meaningful value without explicitly comparing it with `true` or `false`.

## 3. 🌊 Flow

```text
Value
  ↓
Used in a condition
  ↓
Is it falsy?
 ↙        ↘
Yes        No
 ↓          ↓
false      true
```

Example:

```js
if (value) {
  // truthy
} else {
  // falsy
}
```

## 4. ✍️ Syntax

```js
if (value) {
  // Truthy
}
```

```js
if (!value) {
  // Falsy
}
```

You can also check using `Boolean()`:

```js
Boolean(1);   // true
Boolean(0);   // false
```

## 5. 💻 Example

### Falsy Values

```js
Boolean(false);     // false
Boolean(0);         // false
Boolean("");        // false
Boolean(null);      // false
Boolean(undefined); // false
Boolean(NaN);       // false
```

### Truthy Values

```js
Boolean("Hello"); // true
Boolean("0");     // true
Boolean(1);       // true
Boolean([]);      // true
Boolean({});      // true
```

### Common Real Example

```js
const name = "";

if (name) {
  console.log("Name exists");
} else {
  console.log("Name is empty");
}
```

Output:

```text
Name is empty
```

Because an empty string `""` is **falsy**.

## 6. 🧠 Memory Trick

Remember the main falsy values:

> **False, 0, "", null, undefined, NaN**

### Easy Rule

> **If it is not falsy → it is truthy.**

Especially remember:

```text
[] → Truthy
{} → Truthy
"0" → Truthy
"false" → Truthy
```
