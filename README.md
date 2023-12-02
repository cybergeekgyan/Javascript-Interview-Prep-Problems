# Javascript-Interview-Prep-Problems

#### Javascript Important Topics & Concepts

| Level	| Concepts/Topics |
|-------|--------|
| Beginner| - Variables and Data Types|
| | - Operators and Expressions|
| |- Control Flow (if statements, loops)
| |- Functions and Scope
| |- Arrays and Objects
| |- DOM Manipulation
| |- Events and Event Handling
| |- Basic Asynchronous JavaScript (Callbacks, Promises)
| |- Error Handling
| |- Working with Strings
| |- Working with Dates
| |- Debugging using Browser Developer Tools
| |- Introduction to ES6+ Features (let/const, arrow functions)
| |- Introduction to npm and package management
| Intermediate	| - Closures and Lexical Scoping 
| |- Advanced DOM Manipulation
| |- Fetch API and AJAX
| |- Promises and Asynchronous Patterns
| |- ES6+ Features (destructuring, spread/rest operators)
| |- Modules and Module Bundlers (e.g., Webpack)
| |- Working with JSON
| |- Regular Expressions
| |- Functional Programming Concepts (map, filter, reduce)
| |- Unit Testing (e.g., Jest)
| |- Browser Storage (localStorage, sessionStorage)
| |- Responsive Design and Media Queries
| Advanced	| - Prototypal Inheritance and OOP in JavaScript
| |- Advanced Asynchronous Patterns (Async/Await)
| |- Web Components and Shadow DOM
| |- Service Workers and Progressive Web Apps (PWAs)
| |- Reactive Programming (e.g., RxJS)
| |- TypeScript (optional static typing for JavaScript)
| |- Memory Management and Performance Optimization
| | - Design Patterns in JavaScript
| |- Security Best Practices (e.g., Cross-Site Scripting)
| |- Node.js and Server-Side JavaScript
| |- Frameworks and Libraries (e.g., React, Angular, Vue.js)
| |- Building and Deploying JavaScript Applications


### Functional Inheritance

Functional inheritance is the process of receiving features by applying an augmenting function to an object instance. The function supplies a closure scope which you can use to keep some data private. The augmenting function uses dynamic object extension to extend the object instance with new properties and methods.

They look like:

```js
// Base function
function Drinks(data) {
  var that = {}; // Create an empty object
  that.name = data.name; // Add it a "name" property
  return that; // Return the object
};

// Fuction which inherits from the base function
function Coffee(data) {
  // Create the Drinks object
  var that = Drinks(data);
  // Extend base object
  that.giveName = function() {
    return 'This is ' + that.name;
  };
  return that;
};

// Usage
var firstCoffee = Coffee({ name: 'Cappuccino' });
console.log(firstCoffee.giveName());
// Output: "This is Cappuccino"
```

### .map() Substitute

.map() also has a substitute that we can use which is .from():
```Js
let dogs = [
    { name: ‘Rio’, age: 2 },
    { name: ‘Mac’, age: 3 },
    { name: ‘Bruno’, age: 5 },
    { name: ‘Jucas’, age: 10 },
    { name: ‘Furr’, age: 8 },
    { name: ‘Blu’, age: 7 },
]


let dogsNames = Array.from(dogs, ({name}) => name);
console.log(dogsNames); // returns [“Rio”, “Mac”, “Bruno”, “Jucas”, “Furr”, “Blu”]
```
### Number to string/string to number

Usually, to convert a string to a number, we use something like this:
```Js
let num = 4
let newNum = num.toString();
```
and to convert a string to a number, we use:
```Js
let num = "4"
let stringNumber = Number(num);
```
but what we can use to code fast is:
```Js
let num = 15;
let numString = num + ""; // number to string
let stringNum = +s; // string to number
```
### Using length to resize and emptying an array

In javascript, we can override a built-in method called **length** and assign it a value of our choice.

Let's look at an example:
```Js
let array_values = [1, 2, 3, 4, 5, 6, 7, 8];  
console.log(array_values.length); 
// 8  
array_values.length = 5;  
console.log(array_values.length); 
// 5  
console.log(array_values); 
// [1, 2, 3, 4, 5]
```
It can also be used in emptying an array, like this:
```Js
let array_values = [1, 2, 3, 4, 5, 6, 7,8]; 
console.log(array_values.length); 
// 8  
array_values.length = 0;   
console.log(array_values.length); 
// 0 
console.log(array_values); 
// []
```
### Swap Values with Array Destructuring.

The destructuring assignment syntax is a JavaScript expression that makes it possible to unpack values from arrays, or properties from objects, into distinct variables. We can also use that to swap values fast, like this:
```Js
let a = 1, b = 2
[a, b] = [b, a]
console.log(a) // result -> 2
console.log(b) // result -> 1
```
### Remove duplicates from an Array

This trick is pretty simple. Let's say, I made an array that is containing numbers, strings, and booleans, but the values are repeating themselves more than once and I want to remove the duplicates. So what I can do is:
```Js
const array = [1, 3, 2, 3, 2, 1, true, false, true, 'Kio', 2, 3];
const filteredArray = [...new Set(array)];
console.log(filteredArray) // [1, 3, 2, true, false, "Kio"]
```
### Short For Loop

You can write less code for a loop like this:
```Js
const names = ["Kio", "Rio", "Mac"];

// Long Version
for (let i = 0; i < names.length; i++) {
  const name = names[i];
  console.log(name);
}

// Short Version
for (let name of names) console.log(name);
```
### Performance

In JS you can  also get the time that the code was executed in like Google does:

![alt text](https://github.com/gyanprakash0221/Javascript-Tips-Tricks-/blob/main/i7ed89oyhcyyjhqirvc6.png)

It looks like this:
```Js
const firstTime = performance.now();
something();
const secondTime = performance.now();
console.log(`The something function took ${secondTime - firstTime} milliseconds.`);
```
