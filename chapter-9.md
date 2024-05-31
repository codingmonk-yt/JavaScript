# Chapter 9

## Conditional Branching in JavaScript: Making Choices in Your Code

This guide explains conditional branching in JavaScript, a fundamental concept for making decisions in your programs. We'll cover the `if` statement, the conditional (ternary) operator (`?`), and best practices for writing clear and concise code.

**What is Conditional Branching?**

Imagine you're writing a program that lets users enter their age. You want to display a different message depending on their age:

* If they're under 18, show "You're too young to enter."
* If they're 18 or older, show "Welcome!"

This is where conditional branching comes in. It allows your code to choose between different paths based on a condition.

**The `if` Statement:**

The `if` statement is the workhorse of conditional branching in JavaScript. Here's the basic syntax:

```javascript
if (condition) {
  // Code to execute if the condition is true
}
```

- `condition`: This is an expression that evaluates to either `true` or `false`.
- `code block`: This is the code that gets executed only if the `condition` is `true`. The code block needs to be enclosed in curly braces `{}` even if it's just one line.

**Example:**

```javascript
let age = prompt("Enter your age:");

if (age >= 18) {
  alert("Welcome!");
} else {
  alert("You're too young to enter.");
}
```

In this example:

1. The user enters their age using `prompt`.
2. The `if` statement checks if `age` is greater than or equal to 18 (`age >= 18`).
3. If the condition is `true` (age is 18 or older), the code inside the first curly braces (`alert("Welcome!")`) executes.
4. If the condition is `false` (age is under 18), the code inside the `else` block (`alert("You're too young to enter.")`) executes.

**Boolean Conversion:**

JavaScript automatically converts certain values to `true` or `false` before evaluating an `if` statement:

* `true`, non-zero numbers, and non-empty strings are converted to `true`.
* `false`, 0, the empty string `""`, `null`, and `undefined` are converted to `false`.

**The `else if` Statement:**

Sometimes, you need to check multiple conditions. You can chain `if` statements together with `else if`:

```javascript
if (condition1) {
  // code for condition1
} else if (condition2) {
  // code for condition2
} else {
  // code if neither condition is true
}
```

**Example:**

```javascript
let grade = prompt("Enter your grade (A-F):");

if (grade === "A") {
  alert("Excellent!");
} else if (grade === "B") {
  alert("Great job!");
} else if (grade === "C") {
  alert("You did okay.");
} else {
  alert("You need to study harder.");
}
```

**The Conditional (Ternary) Operator (`?`)**

The conditional operator (`?`) provides a shorthand way to assign a value based on a condition. It has three parts:

```javascript
condition ? value_if_true : value_if_false
```

- The `condition` is evaluated.
- If the `condition` is `true`, `value_if_true` is returned.
- If the `condition` is `false`, `value_if_false` is returned.

**Example:**

```javascript
let message = (age >= 18) ? "Welcome!" : "You're too young to enter.";
alert(message);
```

This code achieves the same outcome as the first `if` statement example, but in a single line (though it can become less readable for complex conditions).

**Best Practices:**

* Use clear and meaningful variable names.
* Use proper indentation to make your code readable.
* Use curly braces `{}` for code blocks even if they have only one line.
* Break down complex conditions into smaller, easier-to-understand ones using multiple `if` statements or `else if` statements.
* For simple assignments based on conditions, the conditional operator (`?`) can be a good choice, but prioritize readability for more intricate logic.

By following these guidelines, you can write clear and efficient conditional branching code in JavaScript!
