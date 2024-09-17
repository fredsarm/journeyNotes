# 1. Introduction to JavaScript
## 1.1 What is JavaScript?

JavaScript is a high-level, interpreted programming language that, along with HTML and CSS, powers interactive web experiences. It is used for tasks such as:

- creating dynamic content,
- controlling multimedia,
- animating images,
- managing data on web pages without requiring a page reload,
- developing desktop applications,
- form validation,
- game development,
- IoT projects.
## 1.2 History and Evolution of JavaScript

- **Creation date:** 1995
- **Creator:** Brendan Eich, while working at Netscape Communications
- **Time spent in creation:** 10 days
- **Previous names:** _Mocha_, _LiveScript_, and finally _JavaScript_
- Despite its name, JavaScript is not directly related to Java.
## 1.3 Standardization (**ECMAScript**)

- **ES1 (1997)**
    
    - The first official specification.
    - Aimed to unify different browser implementations of JavaScript, beginning a formalized development process to ensure its evolution in a more controlled and collaborative manner.
- **ES3 (1999)**
    
    - Introduced important features, such as:
        - Regular expressions
        - Improved string handling.
- **ES5 (2009)**
    
    - Introduced features such as:
        - Strict mode
        - JSON support
        - Many other crucial updates that helped modernize JavaScript for web development.
- **ES6 (2015) (ECMAScript 2015)**
    
    - One of the most significant updates, introducing features like:
        - Classes
        - Modules
        - Arrow functions
        - Template literals
        - `let` and `const` keywords.
- **ES7 (2016)**
    
    - Introduced features such as:
        - The exponentiation operator (`**`)
        - The `Array.prototype.includes()` method.
- **ES8 (2017)**
    
    - Added key features like:
        - Async functions
        - `Object.entries()` and `Object.values()` methods.
- **ES9 (2018)** and Beyond:
    
    - Each version continues to refine the language, adding new features like:
        - Optional chaining (ES2020)
        - Nullish coalescing (ES2020).

## 1.4 Frameworks and Libraries

In the 2000s:

- **jQuery** revolutionized JavaScript by simplifying DOM manipulation, making web development more accessible.

In the 2010s:

- Popular frameworks emerged, shaping modern web development:
    - **React**
    - **Angular**
    - **Vue.js**

In 2009:

- **Node.js** brought JavaScript to the server side, enabling full-stack development using a single language for both front-end and back-end.

## 1.4 JavaScript Today

Today, JavaScript is ubiquitous and used in:

- Simple websites and complex web applications
- Mobile apps
- Server-side services
- Desktop applications
## 1.5 How is JavaScript Executed?

JavaScript is executed by specialized software called **JavaScript engines**, which convert the code into machine-readable instructions that can be processed by a computer's hardware. JavaScript engines are embedded in web browsers and environments like Node.js, enabling it to run both on the client (browser) and server (backend).
- **In browsers**: JavaScript interacts directly with the **Document Object Model (DOM)** to create interactive web experiences. This allows JavaScript to 
	- manipulate HTML elements, 
	- handle events, 
	- interact with APIs to make web pages dynamic.
- **In Node.js**: On the server side, Node.js uses the V8 engine to provide APIs for:
	- file handling, 
	- database interaction, 
	- networking. 
### JavaScript Engines (V8, SpiderMonkey, etc.)

In the browser and in server-side:
- **V8**: Developed by Google, V8 powers Google Chrome and Node.js, known for its speed due to Just-In-Time (JIT) compilation, which turns JavaScript into machine code before execution.
In the browser:
- **SpiderMonkey**: The first JavaScript engine, developed by Mozilla, is used in the Firefox browser.
- **Chakra**: Microsoft’s JavaScript engine for the old Edge browser (pre-Chromium).
- **JavaScriptCore (Nitro)**: Used by Apple’s Safari browser, optimized for performance and low memory consumption.

## 1.6 Ways for running JavaScript Code

There are several ways to execute JavaScript in an HTML document. JavaScript can be placed directly in the HTML or linked as an external file, and can be controlled for when and how it is executed.

### 1.4.1 Inline JavaScript in HTML

JavaScript can be written inline inside the HTML document, either within the `<head>` or `<body>` tags using the `<script>` element.

- **Inside the `<head>`**: Placing JavaScript in the `<head>` runs the code as soon as the browser starts loading the document, but it might block rendering of the page until the script finishes executing.

  Example:
  
  ```html
  <!DOCTYPE html>
  <html>
  <head>
      <title>My First JavaScript</title>
      <script>
          alert("This script runs when the page starts loading!");
      </script>
  </head>
  <body>
      <h1>Hello, World!</h1>
  </body>
  </html>
  ```

- **Inside the `<body>`**: Placing the script at the end of the `<body>` ensures that the HTML content is rendered before the script is executed. This is a common practice to prevent scripts from blocking the rendering of the page content.

  Example:
  
  ```html
  <!DOCTYPE html>
  <html>
  <head>
      <title>My First JavaScript</title>
  </head>
  <body>
      <h1>Hello, World!</h1>
      <script>
          alert("This script runs after the content is rendered.");
      </script>
  </body>
  </html>
  ```

### 1.4.2 Using External .js Files

For better code organization, especially in larger projects, JavaScript is typically written in external files and referenced in the HTML document. This allows for code reuse and keeps the HTML clean.

1. **Create an external JavaScript file** (e.g., `script.js`):

   ```javascript
   alert("Welcome to my first JavaScript program!");
   ```

2. **Link the external file in the HTML** using the `<script>` tag with the `src` attribute:

   ```html
   <!DOCTYPE html>
   <html>
   <head>
       <title>My First JavaScript</title>
       <script src="script.js"></script>
   </head>
   <body>
       <h1>Hello, World!</h1>
   </body>
   </html>
   ```

This method helps keep the HTML cleaner and the JavaScript modular, facilitating maintenance and updates.

### Scripts with `defer` and `async`

When using external scripts, you can optimize when they are executed using the `defer` and `async` attributes:

- **`defer`**: This attribute ensures that the script is executed after the entire HTML document has been parsed, but without blocking the downloading of other resources. This is useful when you want your script to interact with elements that are loaded later in the page.

   Example:
   ```html
   <head>
       <script src="script.js" defer></script>
   </head>
   <body>
       <h1>Hello, World!</h1>
   </body>
   ```

- **`async`**: This attribute downloads the script asynchronously and executes it as soon as it is ready, without waiting for the HTML document to finish loading. It is ideal for scripts that don't rely on the content of the page, like analytics or tracking scripts.

   Example:
   ```html
   <head>
       <script src="analytics.js" async></script>
   </head>
   <body>
       <h1>Hello, World!</h1>
   </body>
   ```

Using these attributes helps improve page load times and performance by controlling how scripts are loaded and executed, avoiding the blocking of rendering.

## Summary

JavaScript can be executed inline in the HTML within the `<head>` or `<body>`, or through external files. Inline scripts in the `<head>` execute as the page loads, while scripts at the end of the `<body>` execute after the content has rendered. External scripts keep code organized and can be optimized with the `defer` and `async` attributes, improving the performance and loading behavior of web pages.

# 2. JavaScript Basics

## 2.1 Introduction
JavaScript is a versatile, dynamic programming language that operates as the core of modern web development. To effectively use JavaScript, it is crucial to understand its foundational elements, such as syntax, data types, variables, operators, and control structures. 

## 2.2 Basic Syntax

JavaScript’s syntax is relatively easy to learn, with familiar elements like variables, functions, and control structures. It follows a syntax similar to other C-based languages (such as C++, Java, and C#), making it approachable for many developers. A typical JavaScript program consists of **statements** that perform actions, **variables** that store data, **functions** that encapsulate reusable code, and **control structures** that dictate the flow of execution based on conditions.

JavaScript is case-sensitive and follows a **line-by-line execution model**, where statements are typically ended with semicolons (though **this is optional** due to automatic semicolon insertion). The language also supports **comments**, allowing developers to write explanatory notes within the code.

### 2.1.1 Statements and Declarations
Statements in JavaScript are individual instructions that the browser executes. They can include expressions, variable declarations, and function calls. 

### 2.1.2 Comments
Comments are non-executable lines of text meant to explain or describe code logic. JavaScript supports two types of comments:
- **Single-line comments**: Prefixed with `//`.
- **Multi-line comments**: Wrapped between `/* */`.

### 2.1.3 Control Structures
Control structures manage the flow of a program by allowing the execution of code to change based on conditions or iterations.

#### 2.1.3.1 Conditionals (if, else, switch)
JavaScript supports conditional statements that allow code to execute only if certain conditions are met. These include `if`, `else`, and `switch` statements for multiple conditions.

#### 2.1.3.2 Loops (for, while, do-while)
Loops enable the execution of code repeatedly based on certain conditions, using structures like `for`, `while`, and `do-while` loops.

## 2.3 Data Types

### 2.2.1 Introduction
JavaScript supports various **data types** used to store and manipulate values. Data types are either **primitive** or **non-primitive** (objects).
### 2.2.2 Primitive Types
#### 2.2.2.1 Introduction
Primitive types represent the most basic types of data. They are immutable, meaning their values cannot be changed after they are created.
#### 2.2.2.2 Number
The `Number` type represents both integer and floating-point numbers.
#### 2.2.2.3 String
Strings are sequences of characters enclosed in single or double quotes.
#### 2.2.2.4 Boolean
Booleans represent logical entities and can have two values: `true` or `false`.
#### 2.2.2.5 Undefined and Null
`Undefined` is a variable that has been declared but not assigned a value. `Null` represents the intentional absence of any object value.
#### 2.2.2.6 Symbol (ES6)
**Symbols** were introduced in ES6 (ECMAScript 2015) as a new primitive data type. Unlike other primitive types such as strings or numbers, **Symbols** are unique and immutable, making them ideal for use as unique property keys in objects.
##### Key Characteristics of Symbols:
- **Uniqueness**: Each symbol is guaranteed to be unique, even if two symbols are created with the same description. For example:
 
  ```javascript
  let sym1 = Symbol('description');
  let sym2 = Symbol('description');
  console.log(sym1 === sym2); // false
  ```

  In this example, even though both symbols have the same description, they are different and unique.
- **Immutability**: Once a symbol is created, its value cannot be changed. It remains constant throughout the lifetime of the program.
- **Use as Property Keys**: Symbols are often used as property keys in objects. Since they are unique, they prevent property name collisions, especially in cases where different parts of the code might unintentionally use the same property names. This is particularly useful when working with libraries or frameworks where properties might be added dynamically.
  Example of using symbols as object keys:
  
  ```javascript
  let sym = Symbol('uniqueKey');
  let obj = {
      [sym]: 'value'
  };
  console.log(obj[sym]); // 'value'
  ```

  This ensures that no other code can accidentally override or access this property unless it has a reference to the specific symbol.
  See [[The Use Of Square Brackets to Evaluate Expressions]]
##### Global Symbol Registry:
JavaScript also provides a **global symbol registry**, where you can register and reuse symbols across your application. This allows symbols with the same key to refer to the same symbol:

```javascript
let globalSym1 = Symbol.for('sharedKey');
let globalSym2 = Symbol.for('sharedKey');
console.log(globalSym1 === globalSym2); // true
```

In the example above, both symbols are identical because they were retrieved from the global registry using the `Symbol.for()` method.

- **Symbol.keyFor()**: You can retrieve the key for a symbol in the global registry using `Symbol.keyFor()`:

  ```javascript
  let sym = Symbol.for('sharedKey');
  console.log(Symbol.keyFor(sym)); // 'sharedKey'
  ```

##### Well-Known Symbols:
JavaScript also provides **well-known symbols**, which are predefined symbols used internally by JavaScript to customize object behavior. These include symbols like:
- `Symbol.iterator`: Defines the default iterator for an object.
- `Symbol.toPrimitive`: Defines a function that converts an object to a primitive value.
- `Symbol.toStringTag`: Customizes the default description for an object’s `toString()` method.

Example of `Symbol.iterator`:
```javascript
let iterableObj = {
    *[Symbol.iterator]() {
        yield 1;
        yield 2;
        yield 3;
    }
};

for (let value of iterableObj) {
    console.log(value); // 1, 2, 3
}
```

In summary, **Symbols** add a layer of uniqueness and flexibility to JavaScript, especially for use cases where you need to create non-colliding, hidden object properties or customize behavior using well-known symbols.

#### 2.2.2.7 BigInt (ES2020)
BigInt is a numeric data type that can represent integers with arbitrary precision, useful for working with large numbers beyond the limit of the `Number` type.

### 2.2.3 Non-Primitive Types

Non-primitive types, also known as **objects**, are mutable and can store collections of data or more complex entities.

#### 2.2.2.1 Objects
Objects are key-value pairs where each key (or property) points to a value (which can be a primitive or another object).

#### 2.2.2.2 Arrays
Arrays are ordered lists of values that can be accessed by their index.

#### 2.2.2.3 Functions
Functions are reusable blocks of code that perform a specific task when called.

## 2.4 Variables and Constants

Variables in JavaScript store data values that can be accessed and manipulated throughout the program. Constants are values that are set once and cannot be reassigned.

### 2.3.1 Declaring with var, let, and const
JavaScript provides three ways to declare variables: `var`, `let`, and `const`. 
- **`var`**: The traditional way to declare variables (function-scoped).
- **`let`**: A block-scoped variable declaration introduced in ES6.
- **`const`**: A block-scoped variable that cannot be reassigned after its initial value is set.

### 2.3.2 Scope (global, local, block)
Scope refers to the context in which a variable is accessible. JavaScript has global, local (function), and block-level scope.

### 2.3.3 Hoisting
Hoisting is JavaScript's default behavior of moving declarations to the top of the current scope, allowing variables and functions to be used before they are declared.

## 2.5 Operators

Operators are used to perform operations on variables and values.

### 2.4.1 Arithmetic
Arithmetic operators are used to perform mathematical calculations, such as `+`, `-`, `*`, and `/`.

### 2.4.2 Comparison
Comparison operators, like `==`, `===`, `!=`, and `>`, are used to compare two values.

### 2.4.3 Logical
Logical operators, such as `&&`, `||`, and `!`, are used to combine or invert boolean values.

### 2.4.4 Assignment
Assignment operators, like `=`, `+=`, and `-=`, are used to assign values to variables.

### 2.4.5 Bitwise Operators
Bitwise operators perform operations on the binary representations of numbers, such as `&`, `|`, `^`, and `~`.

## 2.6 Type Coercion

Type coercion refers to the automatic or explicit conversion of values from one data type to another in JavaScript.

### 2.5.1 Implicit and Explicit Coercion
- **Implicit coercion** occurs when JavaScript automatically converts types during operations (e.g., converting a string to a number).
- **Explicit coercion** is when the programmer manually converts a value using methods like `Number()`, `String()`, or `Boolean()`.

---

This section provides an overview of JavaScript's fundamental concepts and prepares you to write functional code by understanding its basic building blocks.

# 3. Functions
## 3.1 Function declaration and expression
## 3.2 Anonymous functions
## 3.3 Parameters and arguments
## 3.4 Callback functions
## 3.5 Recursive functions
## 3.6 Function scope
## 3.7 Closures
## 3.8 Higher-order functions
 ### 3.9 IIFE (Immediately Invoked Function Expression)
 ### 3.10 Asynchronous functions (async/await)

# 4. Objects
## 4.1 Object definition
## 4.2 Properties and methods
## 4.3 Manipulating objects
### 4.3.1 Adding, modifying, and deleting properties
## 4.4 Prototype chain
## 4.5 Prototypal inheritance
## 4.6 Object.create() and Object.assign()
## 4.7 Classes (ES6)
### 4.7.1 Constructors
### 4.7.2 Class methods
### 4.7.3 Inheritance with extends
### 4.7.4 Static methods
## 4.8 This and its context
### 4.8.1 Bind, Call, Apply

# 5. Arrays
## 5.1 Declaring and manipulating arrays
## 5.2 Native array methods
### 5.2.1 push(), pop(), shift(), unshift()
### 5.2.2 map(), filter(), reduce(), forEach()
### 5.2.3 find(), findIndex(), includes()
## 5.3 Multidimensional arrays
## 5.4 Iterating over arrays (for, for...of, forEach)

# 6. DOM Manipulation (Document Object Model)
## 6.1 What is the DOM?
## 6.2 Selecting elements
### 6.2.1 querySelector() and querySelectorAll()
### 6.2.2 getElementById(), getElementsByClassName(), etc.
## 6.3 Modifying elements
### 6.3.1 Altering text and attributes
### 6.3.2 Adding and removing classes
## 6.4 Creating and removing elements
## 6.5 DOM events
### 6.5.1 Adding events (addEventListener)
### 6.5.2 Keyboard, click, and mouse events
### 6.5.3 Event propagation and delegation

# 7. Asynchronous Programming
## 7.1 What is asynchronous programming?
## 7.2 Callbacks and "Callback Hell"
## 7.3 Promises
### 7.3.1 Chaining promises (then/catch)
### 7.3.2 Promise.all() and Promise.race()
## 7.4 Async/Await
## 7.5 Handling asynchronous errors

# 8. JavaScript Modules
## 8.1 What are modules?
## 8.2 Native modules (ES6+)
### 8.2.1 Import and Export
## 8.3 Modules in Node.js
### 8.3.1 CommonJS (require/export)
### 8.3.2 NPM (Node Package Manager)

# 9. JavaScript in Frontend Development
## 9.1 Interaction with HTML and CSS
## 9.2 Handling events
## 9.3 Form validation
## 9.4 Animations with JavaScript
## 9.5 Browser APIs
### 9.5.1 LocalStorage and SessionStorage
### 9.5.2 Fetch API
### 9.5.3 Geolocation API
### 9.5.4 WebSockets
## 9.6 Introduction to jQuery (optional)

# 10. JavaScript in Backend Development (Node.js)
## 10.1 Introduction to Node.js
### 10.1.1 What is Node.js?
### 10.1.2 Event loop and single-threaded model
## 10.2 Building servers with HTTP and Express.js
## 10.3 File manipulation (File System API)
## 10.4 Connecting to databases
### 10.4.1 MySQL, PostgreSQL, MongoDB
## 10.5 WebSockets in Node.js
## 10.6 Authentication and authorization
### 10.6.1 JWT (JSON Web Tokens)
### 10.6.2 OAuth

# 11. Advanced JavaScript
## 11.1 Understanding scope and context (lexical and dynamic)
## 11.2 Memory management and performance
### 11.2.1 Garbage collection
### 11.2.2 Optimizing loops and recursion
## 11.3 Design patterns
### 11.3.1 Singleton
### 11.3.2 Factory
### 11.3.3 Module pattern
## 11.4 Functional programming
### 11.4.1 Pure functions
### 11.4.2 Immutability
### 11.4.3 Function composition
## 11.5 ES6+ and beyond: New JavaScript features
### 11.5.1 Let and Const
### 11.5.2 Arrow functions
### 11.5.3 Destructuring
### 11.5.4 Rest/Spread operators
### 11.5.5 Classes
### 11.5.6 Async/Await
### 11.5.7 Optional chaining and nullish coalescing
## 11.6 State management in large applications
### 11.6.1 Unidirectional data flow
### 11.6.2 Redux, MobX

## 12. JavaScript Testing
## 12.1 Types of tests (Unit, Integration, e2e)
## 12.2 Testing tools
### 12.2.1 Jest
### 12.2.2 Mocha and Chai
### 12.2.3 Cypress for e2e testing
## 12.3 TDD (Test-Driven Development)

## 13. JavaScript Security
## 13.1 Frontend security
### 13.1.1 XSS (Cross-Site Scripting)
### 13.1.2 CSRF (Cross-Site Request Forgery)
## 13.2 Backend security
### 13.2.1 SQL Injection
### 13.2.2 Secure session management
### 13.2.3 Encryption (bcrypt, hash)
