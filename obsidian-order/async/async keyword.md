![[async-keyword.jpg]]

***
![[async-keyword2.jpg]]
***
The **async** keyword is used to declare an asynchronous function. When a function is marked with **async**, it automatically returns a Promise. If the function returns a value, the Promise resolves with that value. If the function throws an error, the Promise is rejected with that error.
 ```javascript
 const fetch = require("node-fetch"); async function asyncFunction() { return 'Hello, async!'; } asyncFunction() .then((result) => console.log(result)) // "Hello, async!" .catch((error) => console.error(error));
```

#async #keyword 