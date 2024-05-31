# Chapter 10

**Logical Operators in JavaScript**

Logical operators are fundamental building blocks in JavaScript for making decisions based on multiple conditions. They allow you to combine boolean expressions (`true` or `false`) to create more complex logic. Here's a breakdown of the four primary logical operators:

**1. OR (||)**

- Represented by two vertical pipes `||`.
- Returns `true` if **at least one** operand is `true`.
- Returns `false` only if **all** operands are `false`.
- **Behavior with Non-Boolean Values:**
    - JavaScript attempts to convert operands to boolean before evaluation.
    - Numbers other than `0` are converted to `true`.
    - `0`, `""` (empty string), `null`, and `undefined` are converted to `false`.
- **Short-Circuit Evaluation:**
    - The OR operator stops evaluating operands as soon as it encounters a `true` value, improving efficiency.

**Examples:**

```javascript
alert(true || false);    // true (at least one operand is true)
alert(1 || 0);           // true (1 is converted to true)
alert("" || "hello");    // "hello" (the first non-falsy value)
alert(false || false);  // false (both operands are false)
```

**2. AND (&&)**

- Represented by two ampersands `&&`.
- Returns `true` only if **all** operands are `true`.
- Returns `false` if **any** operand is `false`.
- **Short-Circuit Evaluation:**
    - Similar to OR, AND stops evaluating operands after encountering a `false` value.

**Examples:**

```javascript
alert(true && true);    // true (all operands are true)
alert(1 && 0);           // false (0 is converted to false)
alert("" && "hello");    // "" (the first falsy value)
alert(false && true);  // false (any operand is false)
```

**3. NOT (!)**

- Represented by an exclamation mark `!`.
- Inverts the boolean value of its operand.
- `!true` evaluates to `false`.
- `!false` evaluates to `true`.
- Can be used for type coercion (converting a value to boolean).

**Examples:**

```javascript
alert(!true);  // false
alert(!false); // true
alert(!0);     // true (0 is falsy)
alert(!1);     // false (1 is truthy)
alert(!!null); // false (double NOT for type coercion)
```

**4. Nullish Coalescing (??)** (Introduced in ES2020)

- Represented by two question marks `??`.
- Provides a default value if the left operand is `null` or `undefined`.
- Otherwise, returns the left operand's value.

**Examples:**

```javascript
let userName = null;
let defaultName = "Guest";
let greeting = userName ?? defaultName; // greeting will be "Guest"
userName = "John";
greeting = userName ?? defaultName; // greeting will be "John"
```

**Best Practices:**

- Use clear and meaningful variable names to enhance code readability.
- Employ proper indentation to structure your conditional logic.
- Consider using parentheses for complex expressions to improve clarity.
- Choose the appropriate operator based on the desired outcome:
    - OR (`||`) for checking whether any condition is true.
    - AND (`&&`) for ensuring all conditions hold true.
    - NOT (`!`) for inverting a boolean value or type coercion.
    - Nullish Coalescing (`??`) for providing a default value in case of `null` or `undefined`.
- Strive for a balance between conciseness and readability.

By effectively utilizing logical operators, you can construct robust control flow within your JavaScript programs.
