

Symbols are a unique data type introduced in ES6. They’re used as identifiers for object properties and are guaranteed to be unique, preventing naming collisions.

Here’s an example of creating and using a symbol:

```javascript
const mySymbol = Symbol('mySymbol'); const obj = { [mySymbol]: 'Hello, World!', }; console.log(obj[mySymbol]); // Output: Hello, World!
```



#js #symbols #javascript 