---
title: "How to Learn Javascript Faster"
datePublished: Sat Oct 14 2023 18:40:29 GMT+0000 (Coordinated Universal Time)
cuid: clnqduqtw000d09jufhv51xy1
slug: how-to-learn-javascript-faster
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1697304710068/644a8a5d-d1db-4ff2-af0e-3b99127c7532.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1697308790445/a774f977-eb39-4764-8e99-833d903075f4.png
tags: blogging, web-development, opensource, hashnode, wemakedevs

---

Our JavaScript Blog will help you to learn the fundamentals of JavaScript scripting language, from the basic to advanced topics step-by-step. If you're a beginner, start with the basics and gradually move forward by learning a little bit every day.

JavaScript is the most popular and widely used client-side scripting language. Client-side scripting refers to scripts that run within your web browser. JavaScript is designed to add interactivity and dynamic effects to web pages by manipulating the content returned from a web server.

## Table of Contents About JavaScript

what is covered in this blog?

* Fundamental Programming Concepts
    
* Data Type
    
* Operator
    
* Using Variables
    
* Generating output
    

### .Fundamental Programming Concepts.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697307220022/9b336ad7-0653-4a12-82d7-b0b042091447.png align="center")

## **Adding JavaScript to Your Web Pages**

There are typically three ways to add JavaScript to a web page:

* Embedding the JavaScript code between a pair of `<script>` and `</script>` tag.
    
* Creating an external JavaScript file with the `.js` extension and then load it within the page through the `src` attribute of the `<script>` tag.
    

Placing the JavaScript code directly inside an HTML tag using special tag attributes such as `onclick`, `onmouseover`, `onkeypress`, `onload`, etc.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697307440785/1e227755-51d0-4d87-820b-618a213d68be.png align="center")

## Data type basically means that which kind of data is stored in a program.

### There are three types of Data type used in the Javascript programming language

1. Primitive data type
    
2. non-primitive data type
    
3. special data type
    

# Primitive Data Types in JavaScript

Primitive data types in JavaScript are:

* `String`: Represents textual data.
    
* `Number`: Represents numeric data. Both integer and floating point numbers are Numbers.
    
* `Boolean`: Represents either `true` or `false`.
    
* `Undefined`: Represents a lack of existence of a variable.
    
* `Null`: Represents the intentional absence of a value.
    

These are called primitive because they represent a single value. They are immutable and have a primitive (basic) type.

## Non-Primitive Data Types

Non-primitive data types are:

* `Object`: Represents a collection of properties. Objects are mutable and can be changed.
    
* `Array`: Represents an ordered list of values. Arrays are mutable.
    

These are called non-primitive because they can contain multiple values. They are mutable and represent a reference type.

## Special Data Types

`Undefined` and `Null` are also considered special data types in JavaScript.

## Differences

* Primitive data types have a value, while non-primitives have a reference.
    
* Primitive types are immutable, while non-primitives are mutable.
    
* Primitive types are passed by value, while non-primitives are passed by reference.
    
* Primitive types have a primitive type, while non-primitives have a reference type.
    

```js
let str = "Hello"; // Primitive data type - String
let arr = [1, 2, 3]; // Non-primitive data type - Array
let num = 5; // Primitive data type - Number
let obj = { name: "John" }; // Non-primitive data type - Object
```

# Operators in JavaScript

Operators are used to perform operations on variables and values. JavaScript supports the following types of operators:

* Arithmetic operators (+, -, \*, /, etc.)
    
* Assignment operators (=, +=, -=, etc.)
    
* Comparison operators (==, !=, &gt;, &lt;, etc.)
    
* Logical operators (&&, ||, !)
    
* String operators (+ for concatenation)
    
* Ternary operator (? :)
    
* Bitwise operators (&, |, ~, &lt;&lt;, &gt;&gt;, etc.)
    
* Comma operator (,)
    
* Unary operators (delete, typeof, void)
    
* Relational operators (in, instanceof)
    

Some examples:

```js
let x = 5;
let y = 10;

// Arithmetic operators
let sum = x + y; // 15
let diff = x - y; // -5

// Assignment operator
x += 2; // x is now 7

// Comparison operator
let equal = x == y; // false

// Logical operator
let result = x && y; // 10 (returns the last value)

// String operator  
let text = "Hello " + "World!"; // "Hello World!"
```

Operators work with various JavaScript expressions like variables, literals, function calls, etc. They have precedence and are evaluated either from left to right or right to left based on the operator.

Some important operators are:

* Assignment operators - Assign values to variables.
    
* Comparison operators - Compare values and return true or false.
    
* Logical operators - Combine expressions and return true or false.
    
* Arithmetic operators - Perform math operations.
    
* Bitwise operators - Perform bit-level operations on integers.
    
* Ternary operator - A shorthand for if-else statements.
    

# Using Variables in JavaScript

Variables are one of the fundamental building blocks of JavaScript. They allow us to store and manipulate data in our programs.

To use a variable in JavaScript, you first need to declare it using the `let` or `const` keyword:

```js
let name;
const age = 20;
```

Here we have declared a variable `name` using `let` and a variable `age` using `const`.

We can then assign values to variables using the assignment operator `=`:

```js
name = 'John';
```

Now the `name` variable holds the string `'John'`.

We can update variables declared with `let`:

```js
name = 'Jane';
```

But we cannot reassign variables declared with `const`:

```js
age = 21; // Throws an error
```

Variables can store different types of data:

* Numbers: `let age = 20;`
    
* Strings: `let name = 'John';`
    
* Booleans: `let isAdmin = true;`
    
* Arrays: `let hobbies = ['Music', 'Sports'];`
    
* Objects: `let user = { name: 'John', age: 30 };`
    

JavaScript also has dynamic typing, meaning we do not need to specify the type of a variable when declaring it. The type is determined by the value assigned to it.

Some best practices for naming variables:

* Use meaningful names
    
* Use camelCase
    
* Avoid reserved words
    
* Avoid starting with numbers
    
* Use `const` by default, only use `let` if the variable needs to change
    

Here is an example of using variables in practice:

```js
const firstName = 'John';
let lastName = 'Doe';

lastName = 'Smith'; // We can reassign let

console.log(firstName); // John
console.log(lastName); // Smith
```

# Printing in JavaScript

There are several ways to print data in JavaScript:

1. `console.log()` - Print to the browser console:
    

```js
console.log("Hello");
```

This is useful for debugging.

1. `document.write()` - Print directly to the HTML:
    

```js
document.write("<p>Hello</p>");
```

This overwrites the existing HTML though, so use with caution.

1. `innerHTML` - Modify the HTML of an element:
    

```html
<p id="output"></p>

<script>
document.getElementById("output").innerHTML = "Hello"; 
</script>
```

1. `alert()` - Show an alert popup:
    

```js
alert("Hello");
```

This pauses script execution until the alert is dismissed.

1. `window.print()` - Print the entire web page:
    

```js
window.print();
```

This opens the browser's print dialog.

The preferred methods are `console.log()` for debugging and `innerHTML` to modify the DOM. `document.write()` and `alert()` should be avoided in most cases.

You can print:

* Strings:
    

```js
console.log("Hello");
```

* Variables:
    

```js
let name = "John";
console.log(name);
```

* Functions:
    

```js
function greeting() {
  return "Hello!";
}
console.log(greeting());
```

* Objects:
    

```js
const user = {
  name: "John"
};
console.log(user);
```

Hope this helps you thank you!

## <mark>End!!!!</mark>