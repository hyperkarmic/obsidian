Overview: This activity is focused on using the `map` and `filter` methods to solve problems we would previously have used a for loop for. The code is separated into two files, `map.js` and `filter.js`. In `filter.js`, we have an array of numbers `originalArray`, and we apply the `filter()` method to create new arrays based on certain conditions. In `map.js`, we use the `map()` method to create new arrays by transforming each element of the original array.

filter.js:

-   The `filter()` method is used to create new arrays based on certain conditions.
-   In this example, we have an array of numbers called `originalArray`.
-   We use `filter()` to create a new array containing only the even numbers in the original array.
-   We then create a new array containing only the prime numbers in the original array using a custom `isPrime()` function provided.
-   Finally, we create a new array containing only the numbers in the original array larger than 5.

Code Snippets:

Filter for even numbers:

```javascript
const evenNumbers = originalArray.filter(function(data) {
  if (data % 2 === 0) {
    return true;
  }
});

```

Filter for prime numbers:

```javascript
const isPrime = num => {
  for (let i = 2; i < num; i++) {
    if (num % i === 0) return false;
  }
  return num !== 1;
};

const primeArray = originalArray.filter(isPrime);

```

Filter for numbers larger than 5:

```javascript
const moreThan5Array = originalArray.filter(num => num > 5);



```

map.js:

-   The `map()` method is used to create a new array by transforming each element of the original array.
-   In this example, we have an array of numbers called `originalArray`.
-   We use `map()` to create a new array containing each element of the original array tripled.
-   We then create a new array containing the text "even" or "odd" for each element of the original array.

Code Snippets:

Map to triple each element:

```javascript 
const tripledArray = originalArray.map(data => data * 3);
```

Map to determine if each element is "even" or "odd":

```javascript
const oddOrEven = originalArray.map(num => (num % 2 === 0 ? "even" : "odd"));

```
