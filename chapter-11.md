# Chapter 11

**Nullish Coalescing Operator (??) in JavaScript**

The nullish coalescing operator (`??`), introduced in ES2020, offers a concise and elegant way to handle null and undefined values in JavaScript. It provides a default value when the left operand is either `null` or `undefined`. Here's a breakdown of its functionality and use cases:

**Behavior:**

- `result = a ?? b` evaluates to:
    - `a` if `a` is not `null` or `undefined` (defined)
    - `b` if `a` is `null` or `undefined`
- Essentially, it returns the first defined value from the left and right operands.

**Example:**

```javascript
let user;  // user is undefined

alert(user ?? "Anonymous"); // Output: "Anonymous" (user is undefined)

user = "John";

alert(user ?? "Anonymous"); // Output: "John" (user is defined)
```

**Applications:**

1. **Default Value Assignment:**
   - It's particularly useful for assigning default values to variables that might be `null` or `undefined`:

   ```javascript
   let height = null;
   let defaultHeight = 100;

   height = height ?? defaultHeight; // height becomes 100
   ```

2. **Chaining for Default Values:**
   - `??` allows you to chain multiple expressions, selecting the first defined value in the sequence:

   ```javascript
   let firstName = null;
   let lastName = undefined;
   let nickName = "Supercoder";

   let userName = firstName ?? lastName ?? nickName ?? "Anonymous";
   alert(userName); // Output: "Supercoder" (first defined value)
   ```

**Comparison with OR (||):**

- While both `??` and `||` can be used for default values, they have a key distinction:
    - `||` returns the first truthy value, including `false`, `0`, and an empty string (`""`).
    - `??` specifically checks for `null` or `undefined`.
- This difference matters when you want to differentiate between the absence of a value and a valid but potentially zero or falsy value:

   ```javascript
   let height = 0; // Valid zero height

   alert(height || 100); // Output: 100 (height is falsy)
   alert(height ?? 100); // Output: 0 (height is defined)
   ```

**Precedence and Parentheses:**

- `??` has a low precedence (similar to `||`), evaluated after most arithmetic operators (`+`, `-`, `*`, `/`) but before `=`.
- Use parentheses for proper evaluation order when `??` is combined with other operators:

   ```javascript
   let area = (height ?? 100) * (width ?? 50); // Correct calculation
   ```

**Limitations with && and ||:**

- To prevent potential confusion during the transition from `||`, JavaScript disallows using `??` directly with `&&` or `||` without explicit parentheses:

   ```javascript
   let x = 1 && 2 ?? 3; // Syntax error
   ```
   - Use parentheses to clarify precedence:

   ```javascript
   let x = (1 && 2) ?? 3; // Correct evaluation, x = 2
   ```

**Summary:**

The nullish coalescing operator (`??`) simplifies handling `null` and `undefined` values in JavaScript. It provides a clear way to assign default values, chain expressions for fallback options, and distinguish between the absence of a value and valid zero or falsy values. Remember to use parentheses when necessary to ensure the desired evaluation order.
