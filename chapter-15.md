# Chapter 15

## Function Expressions in JavaScript

**Function Expressions**

In JavaScript, functions are not just magical constructs, but special values. We've already seen **Function Declarations**, where a function is defined using the `function` keyword followed by the function name, parameters, and the function body.

```javascript
function sayHi() {
  alert("Hello");
}
```

There's another way to create functions: **Function Expressions**. These allow you to define a function anywhere within an expression.

```javascript
let sayHi = function() {
  alert("Hello");
};
```

Here, we're assigning a new function (created using `function() { ... }`) to the variable `sayHi`. Since the function creation happens within the assignment expression (`let sayHi = ...`), it's called a Function Expression. There's no name after the `function` keyword, which is allowed in Function Expressions.

**Functions as Values**

Remember, functions are values. Let's see how this works:

```javascript
function sayHi() {
  alert("Hello");
}

alert(sayHi); // This shows the function code, not "Hello"
```

The last line shows the function's code representation, not its execution. In JavaScript, functions are values you can work with like other data types.

We can even copy a function to another variable:

```javascript
function sayHi() {
  alert("Hello");
}

let func = sayHi; // Copying the function

func(); // Hello (This works!)
sayHi(); // Hello (This still works)
```

Here, the function is first created and stored in `sayHi`. Then, it's copied to the variable `func`. Now, both `sayHi` and `func` refer to the same function, allowing you to call it using either variable name.

**Callback Functions**

Function Expressions are often used with callbacks. Let's look at an example:

```javascript
function ask(question, yes, no) {
  if (confirm(question)) yes();
  else no();
}

function showOk() {
  alert("You agreed.");
}

function showCancel() {
  alert("You canceled the execution.");
}

ask("Do you agree?", showOk, showCancel);
```

The `ask` function takes three arguments:

* `question`: The question to ask the user.
* `yes`: A function to call if the user clicks "OK".
* `no`: A function to call if the user clicks "Cancel".

We pass `showOk` and `showCancel` functions as arguments to `ask`. These are called **callback functions**. The idea is to pass a function and expect it to be called later based on certain conditions.

Here, `showOk` becomes the callback for "yes" and `showCancel` for "no". We can also use Function Expressions to write shorter code:

```javascript
function ask(question, yes, no) {
  if (confirm(question)) yes();
  else no();
}

ask(
  "Do you agree?",
  function() { alert("You agreed."); },
  function() { alert("You canceled the execution."); }
);
```

Here, functions are defined directly within the `ask` call. They are anonymous (without names) and are not accessible outside of `ask`. This is a common way to use Function Expressions in JavaScript.

**Function Expressions vs. Function Declarations**

Here's a breakdown of the key differences:

**Syntax:**

* **Function Declaration:** Defined as a separate statement.
```javascript
function sum(a, b) {
  return a + b;
}
```
* **Function Expression:** Created within an expression.
```javascript
let sum = function(a, b) {
  return a + b;
};
```

**Creation Timing:**

* **Function Declaration:** Created when the script is parsed, visible throughout the script.
* **Function Expression:** Created when the execution flow reaches them, usable from that point onwards.

**Example:**

```javascript
sayHi("John"); // Error (if Function Expression)

function sayHi(name) {
  alert(`Hello, ${name}`);
}
```

In this case, using a Function Expression would cause an error because the function wouldn't be created yet when it's called.

**Use Cases:**

* **Function Declaration:** Generally preferred for declaring functions beforehand, especially for readability.
* **Function Expression:** Used when a function needs to be created conditionally or dynamically within an expression.

**Summary:**

* Functions are values. They can be assigned, copied or declared in any place of the code.
* If the function is declared as a separate statement in the main code flow, that’s called a “Function Declaration”.
* If the function is created as a part of an expression, it’s called a “Function Expression”.
* Function Declarations are processed before the code block is executed. They are visible everywhere in the block.
* Function Expressions are created when the execution flow reaches them.
