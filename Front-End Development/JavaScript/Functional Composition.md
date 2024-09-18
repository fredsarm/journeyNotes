Technique where you combine several smaller functions to create a new function. The result of the composition is a function that applies the individual functions in sequence, where the result of one function is passed as input to the next. This makes it easier to build more modular, reusable, and maintainable solutions.

### Concept of Functional Composition

The idea comes from mathematics, where the composition of functions \( f(g(x)) \) means applying function \( g(x) \) and then applying function \( f \) to the result. In JavaScript, this can be done with functions that receive and return other functions (*higher-order functions*).

### Basic Example of Functional Composition

Let's imagine two simple functions:

```javascript
const addOne = (x) => x + 1;
const double = (x) => x * 2;
```

If you want to create a new function that applies both functions in sequence (first add 1 and then double the value), you can compose them as follows:

```javascript
const composedFunction = (x) => double(addOne(x));

console.log(composedFunction(2));  // Result: 6
```

Here, the `composedFunction` first applies `addOne` to 2 (which gives 3) and then applies `double` to the result (3 * 2 = 6).

### Abstracting Composition with a Function

To make composition more flexible and reusable, you can create a `compose` function that takes two or more functions as parameters and returns a new function that applies these functions in sequence:

```javascript
const compose = (f, g) => (x) => f(g(x));

const composed = compose(double, addOne);

console.log(composed(2));  // Result: 6
```

In this example, `compose(double, addOne)` creates a new function that does the same as `double(addOne(x))`, making the composition reusable for different combinations of functions.

### Composition with Multiple Functions

Composition can also be extended to multiple functions:

```javascript
const composeMultiple = (...funcs) => (x) => funcs.reduceRight((value, func) => func(value), x);

const result = composeMultiple(double, addOne, Math.sqrt)(16);

console.log(result);  // Result: 6 (√16 = 4; 4 + 1 = 5; 5 * 2 = 10)
```

In this case, the `composeMultiple` function applies the functions from right to left, first applying `Math.sqrt` to 16, then `addOne`, and finally `double`.

### Benefits of Functional Composition

- **Code Reuse**: Smaller functions can be combined to create more complex behaviors without code duplication.
- **Modularity**: Each function has a clear responsibility and can be tested and maintained independently.
- **Readability**: Through composition, you can express the data flow more clearly and concisely, without needing to chain multiple function calls manually.

**Functional composition** is a fundamental concept when talking about functional programming in JavaScript, and it can help create cleaner and more structured code, especially when working with *higher-order functions*.