# Chapter 5

## Interacting with Users in JavaScript

JavaScript provides ways to interact with users through pop-up messages and prompts. Here's a breakdown of three common functions:

**1. alert()**

* Displays a message box with a single "OK" button.
* The user must click "OK" to proceed.
* Use it to display important information or warnings.

**Example:**

```javascript
alert("Hello, world!");
```

**2. prompt()**

* Displays a message box with an input field and "OK" and "Cancel" buttons.
* You can provide a title and an optional default value for the input field.
* Returns the text entered by the user (if they click "OK"), or `null` if they click "Cancel" or press Esc.
* Use it to get user input for things like names, ages, or confirmation.

**Example:**

```javascript
let name = prompt("What is your name?", "Guest");
alert("Hello, " + name + "!");
```

**3. confirm()**

* Displays a message box with a question and "OK" and "Cancel" buttons.
* Returns `true` if the user clicks "OK", `false` otherwise.
* Use it to get confirmation before performing an action.

**Example:**

```javascript
let confirmed = confirm("Are you sure you want to delete this file?");

if (confirmed) {
  alert("File deleted!");
} else {
  alert("Deletion canceled.");
}
```

**Important points:**

* All these functions create modal windows, meaning the user can't interact with the rest of the page until they dismiss the window.
* The exact appearance and location of the windows may vary depending on the browser.
* These functions are simple but effective for basic user interaction.

**In essence:**

Use `alert()` for important messages, `prompt()` to get user input, and `confirm()` to get confirmation before actions. These functions provide a way to make your web pages more interactive and user-friendly.
