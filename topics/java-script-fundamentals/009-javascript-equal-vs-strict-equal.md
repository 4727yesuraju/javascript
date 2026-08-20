# `==` vs `===`

## 1. 📖 Simple English Explanation

`==` and `===` are comparison operators used to check whether two values are equal.

* `==` → **Loose equality** → allows type coercion
* `===` → **Strict equality** → checks value **and** type

Example:

```js id="x9z3qa"
5 == "5"   // true
5 === "5"  // false
```

## 2. 🤔 Why is it Needed?

It is important to know the difference because JavaScript can automatically convert types when using `==`.

Using `===` is generally preferred because it gives **more predictable results**.

## 3. 🌊 Flow

### `==`

```text id="p4k7sd"
Compare values
     ↓
Different types?
     ↓
Yes → Type coercion
     ↓
Compare
```

### `===`

```text id="q8m2lc"
Compare value + type
     ↓
Same type?
   ↙     ↘
 No      Yes
 ↓        ↓
false   Compare value
           ↓
        true / false
```

## 4. ✍️ Syntax

```js id="d2k6vp"
value1 == value2;

value1 === value2;
```

## 5. 💻 Example

### `==` — Loose Equality

```js id="m7c4qa"
console.log(5 == "5");
// true
```

Why?

```text id="2f8xwb"
5 == "5"
 ↓
Type coercion
 ↓
5 == 5
 ↓
true
```

### `===` — Strict Equality

```js id="k3v9ds"
console.log(5 === "5");
// false
```

Why?

```text id="r6j1hz"
5 === "5"
 ↓
Number !== String
 ↓
false
```

### Same Value and Same Type

```js id="b5n8qt"
console.log(5 === 5);
// true

console.log("hello" === "hello");
// true
```

### `null` and `undefined`

```js id="v2m7cx"
console.log(null == undefined);
// true

console.log(null === undefined);
// false
```

`==` considers them equal after coercion, while `===` sees that they are different types.

## 6. 🧠 Memory Trick

Remember:

> **`==` → Compare after conversion 🔄**
> **`===` → Compare exactly 🎯**

### Interview Answer

> **`==` compares values after type coercion, while `===` compares both value and type without type coercion. In modern JavaScript, `===` is generally preferred because it is more predictable.**
