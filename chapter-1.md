## Chapter 1: Hello World!

### What is JavaScript?

JavaScript (JS) is a versatile programming language primarily used to create dynamic and interactive web pages. It adds functionality to static HTML pages, allowing elements to respond to user actions and update content without reloading the entire page. 

Think of JavaScript as the brain behind a website, making it react to your clicks, scrolls, and other interactions. 

### Running Your First JavaScript Code

To get started with JavaScript, we need a way to run our code. While there are various environments, using a web browser is convenient for this introduction.

## Running JavaScript Code

### Where to write JavaScript?

* **Inline Scripts:** You can write JavaScript directly within an HTML page using the `<script>` tag.
* **External Scripts:** For larger scripts, it's recommended to place them in separate `.js` files and link them to your HTML using the `<script>` tag with the `src` attribute.

### `<script>` Tag

* Adds JavaScript code to an HTML page.
* Browser executes the code when it processes the tag.

**Example (Inline Script):**

```html
<!DOCTYPE HTML>
<html>
<body>
  <p>Before the script...</p>
  <script>
    alert('Hello, world!');
  </script>
  <p>...After the script.</p>
</body>
</html>
```

###  Inline Script vs. External Script

* **Inline Scripts:** Used for simple scripts, but can clutter your HTML.
* **External Scripts:** 
    * Better organization for complex scripts.
    * Downloaded and cached by the browser, improving performance for subsequent page loads.

**Example (External Script):**

**HTML:**

```html
<script src="myScript.js"></script>
```

**JavaScript (myScript.js):**

```javascript
alert('Hello from external script!');
```

**Note:**

* A `<script>` tag cannot have both `src` attribute and code within it.

### Key Points

* Use `<script>` tag to add JavaScript to a page.
* `type` and `language` attributes are not required in modern HTML.
* Use external files for complex scripts (`.js` files).
* External scripts improve performance by leveraging browser caching.
