The square brackets around `[sym]` in the object definition are necessary because **Symbols (or any other expressions used as property keys) need to be evaluated dynamically**. In JavaScript, when you use a symbol or any non-literal expression as an object property key, you must use square brackets to tell the interpreter to evaluate the expression and use its result as the key.

Here’s a breakdown of why:

### 1. Literal Object Keys vs. Computed Property Keys

- **Literal property keys**: In JavaScript, when you define an object, properties are usually written as strings or numbers by default:
  
  ```javascript
  let obj = {
      key: 'value'
  };
  ```

  Here, the key is literally `'key'` as a string.

- **Computed property keys**: If you want to use a variable (or an expression) as a key, you need to **compute** the key. This is done using square brackets (`[]`).

  For example:
  
  ```javascript
  let propName = 'key';
  let obj = {
      [propName]: 'value'
  };
  console.log(obj.key); // 'value'
  ```

  In this case, the square brackets tell the JavaScript engine to evaluate `propName` and use its value (`'key'`) as the actual property name. Without the brackets, `propName` would be treated as a literal string `"propName"`.

### 2. Using Symbols as Object Keys

In the case of symbols, this is especially important because symbols are **not strings**. A symbol is a unique and immutable primitive, and it cannot be automatically converted to a string like other types (such as numbers or booleans) when used as a property key. You must use square brackets to explicitly tell JavaScript to evaluate the symbol and use its unique value as the property key:

```javascript
let sym = Symbol('uniqueKey');
let obj = {
    [sym]: 'value' // Computed property key using a symbol
};
console.log(obj[sym]); // 'value'
```

Without the square brackets, JavaScript would treat `sym` as a literal string `"sym"`, which is not what you want. The brackets ensure that JavaScript uses the **value of the symbol** rather than treating it as a literal name.

### Why Symbols Require Computed Property Keys

- **Symbols are unique and cannot be represented as strings.** This is why they require the use of square brackets. If you try to use `sym` directly as a key without brackets, JavaScript would try to interpret it as a literal string key, which is not correct.
  
- **Dynamic nature of the expression**: The square brackets allow for **computed property names**, which means you can dynamically set object keys using variables, expressions, or symbols.

In summary, the square brackets in `[{sym}: 'value']` tell JavaScript that the key is dynamically computed, in this case, using the `sym` symbol, which ensures that the key is not a string, but a unique symbol.