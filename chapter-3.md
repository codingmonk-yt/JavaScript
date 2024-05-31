# Chapter 3

## Variables in JavaScript

**What are variables?**

* Variables are named storage locations for data in your program.
* You can use them to store anything from text to numbers to more complex data structures.

**Declaring variables:**

* Use the `let` keyword to declare a variable.
  * This is the preferred way to declare variables in modern JavaScript.
* Example:

```javascript
let message;
```

**Assigning values to variables:**

* Use the assignment operator (`=`) to assign a value to a variable.
* Example:

```javascript
let message;
message = 'Hello!';
```

**Accessing variable values:**

* Use the variable name to access the value stored in it.
* Example:

```javascript
let message;
message = 'Hello!';

alert(message); // This will show "Hello!"
```

**Declaring multiple variables:**

* You can declare multiple variables on separate lines:

```javascript
let user = 'John';
let age = 25;
let message = 'Hello!';
```

* Or you can declare them on a single line (not recommended for readability):

```javascript
let user = 'John', age = 25, message = 'Hello!';
```

**`var` vs. `let`:**

* You may also see the `var` keyword used to declare variables in older code.
* There are slight differences between `var` and `let`, but we'll cover those later.
* It's generally recommended to use `let` for new code.

**Variable naming:**

* Variable names can contain letters, numbers, underscores (`_`), and dollar signs (`$`).
* The first character cannot be a number.
* Use camelCase (e.g., `userName`) for multi-word names.
* Choose descriptive names that reflect the data the variable holds.

**Constants:**

* Use the `const` keyword to declare a constant variable.
* The value of a constant cannot be changed after it's assigned.
* Use constants for values that should never change.

**Naming conventions for constants:**

* Use uppercase letters and underscores for constants (e.g., `COLOR_RED`).
* This is typically used for values known before the program runs.

**Best practices:**

* Use clear and meaningful variable names.
* Avoid using short or cryptic names.
* Declare a new variable for each distinct value you want to store.
* Don't reuse variables for different purposes.

**Summary:**

* Variables store data in your program.
* Use `let` to declare variables and `=` to assign values.
* Choose descriptive names and use constants when appropriate.
