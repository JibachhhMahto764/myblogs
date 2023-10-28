---
title: "Typescript for Beginners"
datePublished: Thu Oct 05 2023 15:20:06 GMT+0000 (Coordinated Universal Time)
cuid: clndbqd9a000409ij5gmk8zpa
slug: typescript-for-beginners
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1696778060320/69b70343-af6e-421f-9350-acce97174a83.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1696519157713/7f4fd651-2b28-41f2-81a1-f69fa32991cc.png
tags: typescript, learn-coding, typescript-tutorial

---

# Typescript

## Basics

Typescript is a superset of JavaScript that adds static typing and classes to the language. It compiles plain JavaScript that runs in any browser or Node.

Some of the main benefits of Typescript are:

* Catch errors early: Type checking catches errors at compile time rather than runtime.
    
* Better documentation: Types provide intrinsic documentation of your code.
    
* Reusable code: Interfaces and generics promote code reuse.
    
* Tools and IDE support: There are many tools and IDE integrations to help you write Typescript.
    

To use Typescript, you first need to install the Typescript compiler:

```plaintext
npm install -g typescript
```

Then you can compile a `.ts` file to `.js` using:

```plaintext
tsc filename.ts
```

This will generate `filename.js` which you can include in your HTML file.

## Primitives

Typescript has the following primitive types:

* string
    
* number
    
* boolean
    
* null
    
* undefined
    
* symbol (ES2015)
    
* void
    

You can define the type of a variable using a type annotation:

```ts
let name: string = "John";
let age: number = 30; 
let hasJob: boolean = true;
```

## Objects

You can define an object type as:

```ts
let person: {
  name: string;
  age: number;
}

person = {
  name: 'John',
  age: 30
}
```

## Arrays

You can define array types as:

```ts
let names: string[] = ['John', 'Jane'];
let numbers: number[] = [1, 2, 3];
let mixed: (string|number)[] = ['John', 1];
```

## Classes

Classes in TypeScript are similar to JavaScript classes, but they allow you to define types for properties and methods:

```ts
class Person {
  name: string
  age: number
  
  constructor(name: string, age: number) {
    this.name = name;
    this.age = age; 
  }
  
  greet() {
    console.log(`Hello, my name is ${this.name}!`);
  }
}
```

## Functions

You can define the parameter and return types of functions:

```ts
function add(x: number, y: number): number {
  return x + y;
}
```

## Interfaces

Interfaces define the shape of an object:

```ts
interface Person {
  name: string;
  age: number;
}

let john: Person = {
  name: 'John',
  age: 30
}
```

## Modules

TypeScript supports ES2015 modules that compile to CommonJS or AMD modules:

```ts
// person.ts
export interface Person { ... }

// main.ts
import { Person } from './person';
```

Hope this helps give you a basic overview of Typescript for beginners! Let me know if you have any other questions.