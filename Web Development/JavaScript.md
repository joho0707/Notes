# JavaScript

JavaScript is a scripting or programming language for adding functionality to websites

```js
console.log("Hello, World!");
```

Comments in JavaScript are the same as C

```js
//  Single-line comment

/* 
    Multi-line comment
*/
```

## JavaScript vs Java

JavaScript **is NOT** Java; [see here](http://javascriptisnotjava.com/)

Java is general purpose and has many use cases, JavaScript is mainly used for web development

## Linking to a website

We can link a JavaScript file similarly to a CSS file:

```html
<!-- for CSS -->
<link src="style.css">

<!-- for JavaScript -->
<script src="script.js"></script>
```

It is advised to include the script tag **at the end** of the `<head>` tag. This is to ensure the DOM (Document Object Model) is created before the script is loaded.

## Variables

JavaScript is a **dynamically typed** language - you don't have to declare data types

You can declare a variable with 3 different keywords:

- `const` - used to declare **constant (unchanging)** variables; values must be assigned at creation
- `let` - used to declare variables that can change values; only introduced **after 2015**
- `var` - used to declare variables that can change values

**NOTE:** `var` variables have **function scope**; `let` variables have **block scope**; These changes were introduced to prevent very common bugs from scoping

## Functions

Functions are blocks of code designed to solve a certain task.

You can declare a function as such:

```js
function func_name(parameters, ...) {
    // enter code

    return value;
}
```

Functions can be used to repeat code execution without copying the code multiple times.

```js
function print_name(name) {
    console.log("Hello " + name);
}

print_name("Joshua");
print_name("Goon");
print_name("Him");
print_name("david");
```

## Using the DOM
