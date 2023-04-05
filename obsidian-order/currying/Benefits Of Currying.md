**Reusable functions:** Currying allows you to create reusable functions that can be partially applied with some arguments and then used multiple times with different arguments.

```javascript
const add = (a) => (b) => a + b;  
  
const add5 = add(5);  
const add10 = add(10);  
  
console.log(add5(3)); // 8  
console.log(add10(3)); // 13
```

2. **Readability:** Currying can make code easier to read and understand by breaking down complex functions into smaller, more manageable functions.

```javascript
const add = (a) => (b) => (c) => a + b + c;  
  
const add5 = add(5);  
const add5And10 = add5(10);  
  
console.log(add5And10(3)); // 18
```

3. **Composition:** Currying allows you to compose functions together to create new functions, making it easier to write and manage code.

```javascript
const add = (a) => (b) => a + b;  
const multiply = (a) => (b) => a * b;  
  
const add5 = add(5);  
const double = multiply(2);  
  
const doubleAndAdd5 = (x) => add5(double(x));  
  
console.log(doubleAndAdd5(3)); // 11
```

The use of currying in this example makes the code more composable and maintainable by breaking down complex functions into smaller, simpler functions that can be composed together to create the final result.

4. **Easier testing:** Functions that are curried are easier to test, as you can test each individual function in isolation.

5. **Better code organization:** By breaking down functions into smaller, more manageable functions, currying can help to improve the organization of your code.

```javascript
const add = (a) => (b) => a + b;  
const multiply = (a) => (b) => a * b;  
  
const add10 = add(10);  
const multiplyBy5 = multiply(5);  
  
const add10AndMultiplyBy5 = (n) => add10(multiplyBy5(n));  
  
console.log(add10AndMultiplyBy5(2)); // 20
```

The use of currying in this example improves code organization by breaking down the simple `add` and `multiply` functions into smaller, more manageable functions that can be composed together in a single expression to achieve the desired result. This can help to make the code more readable, maintainable, and reusable.

6. **Improved performance:** Currying can lead to improved performance, as partially applied functions can be optimized and cached, reducing the number of function calls and improving performance.

```javascript
const memoizedFetch = (() => {  
  const cache = {};  
  return (url) => {  
    if (cache[url]) return Promise.resolve(cache[url]);  
    return fetch(url)  
      .then((response) => response.json())  
      .then((data) => {  
        cache[url] = data;  
        return data;  
      });  
  };  
})();  
  
const fetchUsers = memoizedFetch("https://jsonplaceholder.typicode.com/users");  
const fetchPosts = memoizedFetch("https://jsonplaceholder.typicode.com/posts");  
const fetchTodos = memoizedFetch("https://jsonplaceholder.typicode.com/todos");  
  
fetchUsers.then(console.log); // [{...}, {...}, ...]  
fetchPosts.then(console.log); // [{...}, {...}, ...]  
fetchTodos.then(console.log); // [{...}, {...}, ...]
```

7. **Better function composition:** When functions are curried, they can be composed in a more flexible way, making it easier to write complex functions and making the code more maintainable.

```javascript
const multiply = (a) => (b) => a * b;  
const add = (a) => (b) => a + b;  
const modulo = (a) => (b) => b % a;  
  
const isOdd = modulo(2);  
const double = multiply(2);  
const increment = add(1);  
  
const processNumber = (num) =>  
  double(increment(isOdd(num) ? num : increment(num)));  
  
console.log(processNumber(2)); // 6  
console.log(processNumber(3)); // 8
```

