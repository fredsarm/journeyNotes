# Introduction:
These are functions that can:
1. Accept other functions as **arguments**.
2. **Return** a function as their result.
- They allow:
    - functions to be treated as values
    - creating dynamic and reusable behaviors.
    - contribute to code flexibility.
- They help in understanding advanced concepts related to functions such as:
    - **[[Functional Composition]]**,
    - **Currying**,
    - **Partial Application**,
    - [[Immutability]],
    - [[Referential transparency]],
    - [[Lazy Evaluation]],
    - [[Recursion]],
    - [[Monad]],
    - [[Side effects]].

# 1. Functions as Arguments
**Example:**

```javascript
function greet(name) {
    return `Hello, ${name}!`;
}

function logGreeting(func, name) {
    console.log(func(name));
}

logGreeting(greet, "Frederico");
```

- The function `greet` receives a name (in the `name` parameter) and returns a greeting.
- The function `logGreeting` receives a function (`func`) and a name (`name`). It then calls the `func` function, passing `name` (preserved in the lexical context) as the argument for the `greet` function.

Example of calling the `logGreeting` function using another function as a parameter, instead of the `greet` function:

```JavaScript
function multilingualGreeting(name) {
    const greetings = [
        `Hola, ${name}!`,   // Spanish
        `Bonjour, ${name}!`, // French
        `Hallo, ${name}!`,   // German
        `Ciao, ${name}!`,    // Italian
        `Olá, ${name}!`      // Portuguese
    ];
    const randomGreeting = greetings[Math.floor(Math.random() * greetings.length)];
    return randomGreeting;
}

logGreeting(multilingualGreeting, "Frederico");
// Output (example): Bonjour, Frederico!
```

# 2. Functions as Return Values

```javascript
function createMultiplier(multiplier) {
    return function(number) {
        return number * multiplier;
    };
}

const double = createMultiplier(2); // A
console.log(double(5));             // B
```

**What happens in step A:** `const double = createMultiplier(2);`

1. **Call to `createMultiplier(2)`**: The argument `2` is assigned to the `multiplier` parameter within this function.
   
2. **Return of a new function**: The `createMultiplier` function returns a new function that expects a `number` parameter. This function still "remembers" the value of `multiplier` that was passed to `createMultiplier`, meaning `multiplier = 2` in this case.

   The returned function looks like this:
   
   ```javascript
   function(number) {
       return number * 2;  // multiplier was "fixed" as 2
   }
   ```
   
   Now, the value of the `double` variable is this new function. The variable is a function that can be called as such.

**What happens in step B:** `console.log(double(5));`

1. **Call to `double(5)`**: Here, you are calling the function assigned to `double`. Since `double` is actually the function returned by `createMultiplier(2)`, you are calling the nested function:
   
   ```javascript
   function(number) {
       return number * 2;
   }
   ```

2. **Passing the argument `5`**: The value `5` is passed as the `number` argument to this function. So, inside the nested function, `number = 5`.
3. **Calculation inside the nested function**: The function now performs the calculation `number * multiplier`, i.e., `5 * 2`, and returns the value `10`.
4. **Final result**: The value `10` is displayed in `console.log`.

### Why does this work?
The "magic" here is the concept of **closures**. 
#### Closure
A **closure** is the combination of the "inner" function with the **context** of the "outer" function, even after the latter has finished executing.
The **context** or **"environment"** (also called **lexical context**) includes variables and parameters that were in the scope of the outer function at the time it was executed.
In the previous example, the `multiplier` parameter, with the value passed as an argument (2) when the `createMultiplier(multiplier)` function was called, integrates the lexical environment of the closure and persists after the function returns.

#### The ***state*** of the closure
##### Extinction of the closure
When the outer function is called, the closure comes into existence with its lexical context. When the inner function is called without being assigned as a value to a variable, this lexical context is used for the execution of the inner function and then is lost.
```JavaScript
function createCounter() {
  let count = 0;  // Initializes the variable at each execution
  return function() {
    count++;
    return count;
  };
}

console.log(createCounter()());  // 1 (new closure, count starts at 0)
console.log(createCounter()());  // 1 (the previous lexical context is lost, so instead of 1, the count starts again at 0)
```

##### Persistence of the closure
By assigning a variable to the outer function, as its value, the lexical context is preserved between calls:
```JavaScript
function createCounter() {
  let count = 0;
  return function() {
    count++;
    return count;
  };
}

const counter = createCounter();  // Stores the closure

console.log(counter());  // 1 (count starts at 0 and is incremented)
console.log(counter());  // 2 (count is preserved and incremented to 2)
console.log(counter());  // 3 (continues from the previous state)
```