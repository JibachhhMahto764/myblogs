---
title: "Top 10 Common Mistakes to Avoid in JavaScript"
datePublished: Wed Oct 25 2023 01:48:05 GMT+0000 (Coordinated Universal Time)
cuid: clo53j5hp000008mjb4rtg87w
slug: top-10-common-mistakes-to-avoid-in-javascript
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1698198381780/6543d3df-f593-42d5-b712-673d7d17b2c0.png
tags: blogging, javascript, web-development, blogswithcc, wemakedevs

---

### ***the beginner should know about***

JavaScript is a powerful language, but it’s also easy to fall into traps that can cause bugs and **it makes it more difficult for you to do something or make progress**. So, let’s dive in and explore the 10 most common mistakes in JavaScript and how you can [**avoid**](https://dictionary.cambridge.org/dictionary/english/avoid) them!

### Javascript Mistake No. 1:- Missing or misplacing semicolons

### `Missing or misplacing semicolons in JavaScript can lead to unexpected syntax errors or unintended behavior. It's important to include semicolons at the end of statements and use them consistently to avoid issues.`

**Missing Semicolons at the End of Statements:**

bad code:

```basic
let a = 5
let b = 10
```

In this example, you have two variable declarations without semicolons at the end. JavaScript may automatically insert semicolons, but it can lead to confusion and errors.

good code:

```basic
let a = 5;
let b = 10;
```

**Misplaced Semicolons:**

bad code:

```basic
let x = 5;;
let y = 10;;
```

In this example, semicolons are placed consecutively, which is not necessary. JavaScript will insert a semicolon at the end of the first line and treat the extra semicolons as empty statements, which won't cause a syntax error.

Good code:

```basic
let x = 5;
let y = 10;
```

### Javascript Mistake No. 2:- Breaking a Javascript String

JavaScript will allow you to break a statement into two lines But breaking a statement in the middle of a string will not work:

bad code:

```basic
let x = "Hello
World!";
```

You must use a "backslash" if you must break a statement in a string:

good code:

```basic
let x = "Hello \
World!";
```

### Javascript Mistake No. 3:- Breaking a Return Statement

In JavaScript, a `return` statement is used to exit a function and optionally return a value. You cannot directly "break" a `return` statement in the middle of the function, as it will immediately exit the function, and any code after the `return` the statement will not be executed.

```basic
function exampleFunction() {
  console.log("Before return");
  return "Hello, world"; // This exits the function immediately
  console.log("After return"); // This code will not be executed
}

console.log(exampleFunction()); // "Before return" will be logged, but "After return" will not.
```

I noticed that the code example you provided doesn't contain any errors. It's a simple function that logs a message before the `return` statement and returns a string. Here it is:

bad code:

```javascript
function exampleFunction() {
  console.log("Before return");
  return "Hello, world";
}

console.log(exampleFunction()); // "Before return" will be logged, and "Hello, world" will be returned and logged.
```

Good code:

```basic
function exampleFunction() {
  console.log("Before return");
  return "Hello, world";
}

console.log(exampleFunction()); // "Before return" will be logged, and "Hello, world" will be returned and logged.
```

### Javascript Mistake No.4 Confusing Adding & Concatenation

**Addition** is about adding **numbers**. **Concatenation** is about adding **strings**. In JavaScript, both operations use the same `+` operator. Because of this, adding a number as a number will produce a different result from adding a number as a string:

bad code:

```basic
let x = 30;
x = 30 + 5;       // Now x is 35

let y = 30;
y += "5";        // Now y is "305"
```

Good code:

When adding two variables, it can be difficult to anticipate the result:

```basic
let x = 20;
let y = 5;
let z = x + y;     // Now z is 25

let x = 20;
let y = "5";
let z = x + y;     // Now z is "205"
```

### Javascript Mistake No.5:-Misunderstanding Variables Scope

In JavaScript, variable scope can be tricky, especially when using `var`. I recommend avoiding `var` and using `let` and `const` instead. These block-scoped declarations will make your code easier to reason about and minimize the risk of unintended variable hoisting.

bad code:

```basic
function printNumbers() {
  for (var i = 0; i < 5; i++) {
    setTimeout(function () {
      console.log(i); // Outputs 5, 5, 5, 5, 5
    }, 1000);
  }
}
```

Good code:

```basic
function printNumbers() {
  for (let i = 0; i < 5; i++) {
    setTimeout(function () {
      console.log(i); // Outputs 0, 1, 2, 3, 4
    }, 1000);
  }
}
```

### Javascript Mistake No.6:-**Neglecting Error Handling**

Error handling is super important when making computer programs. If you don't deal with errors properly, your program might suddenly stop working and make users upset. To handle errors in code that happen one step at a time, you can use something called a "try-catch" block. It's like putting a safety net to catch errors.

bad code:

```basic
fetchData()
  .then((data) => {
    // Processing data
  });
```

good code:

```basic
fetchData()
  .then((data) => {
    // Processing data
  })
  .catch((error) => {
    console.error('Error fetching data:', error);
  });
```

### Javascript Mistake No.7:-Accidentally Using the Assignment Operator

JavaScript programs may generate unexpected results if a programmer accidentally uses an assignment operator (`=`), instead of a comparison operator (`==`) in an if statement. This `if` statement returns `false` (as expected) because x is not equal to 20:

bad code:

```basic
let x = 0;
if (x == 20)
```

This `if` statement returns `true` (maybe not as expected), because 20 is true:

```basic
let x = 0;
if (x = 10)
```

This `if` statement returns `false` (maybe not as expected), because 0 is false:

good code:

```basic
let x = 0;
if (x = 0)
```

### Javascript Mistake No.8:- Undefined is not Null

JavaScript objects, variables, properties, and methods can be `undefined`. In addition, empty JavaScript objects can have the value `null`.

```basic
if (typeof myObj === "undefined")
```

But you cannot test if an object is `null`, because this will throw an error if the object is `undefined`:

bad code:

```basic
if (myObj === null)
```

Good code:

```basic
if (typeof myObj !== "undefined" && myObj !== null)
```

### Javascript Mistake No.9:- Expecting Loose Comparison

comparison with (==)

In regular comparison, data type does not matter. This `if` the statement returns true:

```basic
let x = 10;
let y = "10";
if (x == y)// output is true
```

comparison with (===)

In strict comparison, data type does matter. This `if` the statement returns false:

```basic
let x = 10;
let y = "10";
if (x === y)// output is false
```

## Javascript Mistake No.10:-Explanation Mistakes

If a statement is incomplete like:

```basic
return
```

JavaScript will automatically close it like this:

```basic
return;
```

## Conclusion:-

1. Missing or misplacing semicolons in statements.
    
2. Breaking a JavaScript string without using a backslash for line continuation.
    
3. Misunderstanding the behavior of the `return` statement, which exits a function immediately.
    
4. Confusing addition and concatenation when using the `+` operator.
    
5. Misunderstanding variable scope, especially when using `var`.
    
6. Neglecting error handling in asynchronous code, leading to unexpected crashes.
    
7. Accidentally using the assignment operator (`=`) instead of a comparison operator (`==` or `===`) in `if` statements.
    
8. Failing to distinguish between `undefined` and `null` in conditional checks.
    
9. Relying on the loose comparison (`==`) without considering data types.
    
10. Expecting JavaScript to automatically close incomplete statements.
    

These are common mistakes to be aware of while working with JavaScript. Avoiding these can lead to more reliable and maintainable code.