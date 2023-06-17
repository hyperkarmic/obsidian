
Maps, introduced in ES6, are a collection of key-value pairs. They’re similar to objects, but with some key differences, such as maintaining the insertion order and allowing any data type as a key. Here’s an example of creating and using a map:

```javascript
const myMap = new Map(); myMap.set('name', 'John'); myMap.set('age', 25); console.log(myMap.get('name')); // Output: John console.log(myMap.get('age')); // Output: 25 console.log(myMap.has('name')); // Output: true myMap.delete('name'); console.log(myMap.has('name')); // Output: false
```

#js #javascript #maps