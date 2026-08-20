# Type Conversion

## 1. 📖 Simple English Explanation

**Type Conversion** means changing a value from one data type to another.

For example, converting a **string** `"10"` into a **number** `10`.

There are two types:

* **Explicit Conversion** → We manually convert the type.
* **Implicit Conversion (Coercion)** → JavaScript automatically converts the type.

## 2. 🤔 Why is it Needed?

Type conversion is needed when different data types are used together.

For example, data received from an input field or API is often a **string**, but we may need to perform mathematical operations on it.

```js
const age = "25";

console.log(Number(age) + 5); // 30
```

## 3. 🌊 Flow

### Explicit Conversion

```text id="8k2pfa"
Original Value
      ↓
Conversion Function
      ↓
New Data Type
```

```text
"10"
 ↓ Number()
10
```

### Implicit Conversion

```text id="v4n7cz"
Different Data Types
      ↓
JavaScript automatically converts
      ↓
Operation
      ↓
Result
```

```text
"10" + 5
   ↓
"10" + "5"
   ↓
"105"
```

## 4. ✍️ Syntax

### String → Number

```js id="w6h1qz"
Number("10");
parseInt("10");
parseFloat("10.5");
```

### Number → String

```js id="g3v8ka"
String(10);
(10).toString();
```

### Value → Boolean

```js id="k9d2rx"
Boolean(1);    // true
Boolean(0);    // false
```

## 5. 💻 Example

### Explicit Conversion

```js id="a8m4cf"
const age = "25";

const numberAge = Number(age);

console.log(numberAge);        // 25
console.log(typeof numberAge); // "number"
```

### Implicit Conversion

```js id="q1z7nb"
console.log("5" + 2); // "52"
console.log("5" - 2); // 3
```

Why?

```text id="m6r3ty"
"5" + 2
→ + with string performs string concatenation
→ "52"

"5" - 2
→ - requires numbers
→ "5" becomes 5
→ 5 - 2
→ 3
```

### Common Conversions

```js id="f4p8ws"
Number("10");       // 10
String(10);         // "10"
Boolean(1);         // true

Number("hello");    // NaN
Boolean(0);         // false
Boolean("hello");   // true
```

## 6. 🧠 Memory Trick

Remember:

> **Explicit = You Convert** ✋
> **Implicit = JavaScript Converts** 🤖

Common functions:

```text id="z7c2lm"
Number()  → Number
String()  → String
Boolean() → Boolean
```

**Important:** `+` often converts to **String**, while `-`, `*`, `/` usually convert values to **Number**.
