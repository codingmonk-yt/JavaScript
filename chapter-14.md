# Chapter 14

**Functions: The Building Blocks of JavaScript**

Imagine you need to perform the same task repeatedly throughout your program, like displaying a message when a user logs in or logs out. Functions come in as superheroes here! They are reusable blocks of code that let you avoid writing the same logic over and over again.

**Creating a Function**

Here's how to create a function using a function declaration:

```javascript
function functionName(parameter1, parameter2, ...parameterN) {
  // Code to be executed (function body)
}
```

- `function`: Keyword that tells JavaScript you're defining a function.
- `functionName`: A descriptive name for your function (think action it performs).
- `parameter1, parameter2, ...parameterN`: Optional parameters (inputs) the function can receive. These are separated by commas.
- `// Code to be executed`: The instructions that make up the function's body. These are enclosed in curly braces `{}`.

**Calling a Function**

Once you've defined a function, you can call it (execute it) using its name followed by parentheses:

```javascript
functionName(argument1, argument2, ...argumentN);
```

- `functionName`: The name of the function you want to execute.
- `argument1, argument2, ...argumentN`: Values (arguments) you pass to the function, corresponding to the parameters it accepts. These are also separated by commas.

**Example: Showing a Message**

Let's create a function to display a message:

```javascript
function showMessage(message) {
  alert(message);
}

showMessage("Hello, world!"); // Output: Hello, world!
```

In this example:

- `showMessage` is the function name, indicating it shows a message.
- `message` is the parameter (input) the function takes, which is the message to be displayed.
- `alert(message)` is the function body, which uses the `alert` function to display the provided message.
- `showMessage("Hello, world!")` calls the function, passing "Hello, world!" as the argument (the message to show).

**Local vs. Outer Variables**

- **Local Variables:** Variables declared inside a function are only accessible within that function. They are like private workspaces.
- **Outer Variables:** A function can access variables declared outside of it (in the outer scope), but only if there are no local variables with the same name. Imagine it peeking outside its workspace.

**Example: Local vs. Outer Variables**

```javascript
let userName = "John";

function showMessage() {
  let message = "Hello, " + userName; // Local variable
  alert(message);
}

showMessage(); // Output: Hello, John (uses outer userName)

alert(message); // Error! message is not accessible outside the function
```

**Global Variables (Not Recommended)**

- Variables declared outside of any function are called global variables. They are accessible from anywhere in your code.
- While they can be useful in specific situations, it's generally recommended to minimize their use as they can lead to naming conflicts and make code harder to maintain.

**Parameters and Arguments**

- When you call a function, you can pass values (arguments) to it. These arguments are assigned to the function's parameters (inputs).
- Inside the function, you can use these parameters as if they were local variables.

**Example: Parameters and Arguments**

```javascript
function showMessage(from, text) {
  alert(from + ": " + text);
}

showMessage("Ann", "Hello!"); // Output: Ann: Hello!
showMessage("Ann", "What's up?"); // Output: Ann: What's up?
```

Here, `from` and `text` are the parameters, and "Ann" and "Hello!" or "What's up?" are the arguments passed during the function calls.

**Default Parameters**

- If a function is called without providing a value for a parameter, the parameter's value becomes `undefined`.
- You can specify default values for parameters during the function declaration using `=`:

```javascript
function showMessage(from, text = "no text given") {
  alert(from + ": " + text);
}

showMessage("Ann"); // Output: Ann: no text given (default text used)
```

**Returning a Value**

- A function can return a value back to the code that called it. This value becomes the result of the function call.
- Use the `return` keyword to specify the value to be returned
