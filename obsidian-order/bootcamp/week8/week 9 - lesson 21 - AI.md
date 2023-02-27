The code above is a demonstration of three common methods used in functional programming with arrays in JavaScript. These methods are `forEach`, `filter`, and `map`.

1.  `forEach` is used to iterate through an array and execute a provided function for each element in the array. In the example, the `forEach` function is used to log out the age of each patron in the `moviePatrons` array.
    
2.  `filter` is used to create a new array with all elements that pass a provided test implemented by the provided function. In the example, the `filter` function is used to create a new array containing only patrons whose age is greater than 17. This new array is then logged to the console.
    
3.  `map` is used to create a new array with the results of calling a provided function on every element in the calling array. In the example, the `map` function is used to create a new array with the same number of elements as the `moviePatrons` array. For each element in the array, a new object is created with the same properties as the original object. Then, a new property `canWatchRatedR` is added to the object based on the patron's age. The new array is then logged to the console.
    

The learning outcomes of this exercise are:

-   Understanding how to use `forEach`, `filter`, and `map` in functional programming with arrays in JavaScript
-   Understanding how to iterate through an array without a traditional for-loop
-   Understanding how to create a new array based on elements of an existing array using a provided function

Below are some key code snippets with explanations:

1.  Using `forEach` to log out each patron's age:

```javascript
moviePatrons.forEach(patron => console.log(patron.age));

```

In this code, `forEach` is called on the `moviePatrons` array. The provided function logs out the `age` property of each `patron` object in the array.

2.  Using `filter` to create a new array of patrons who can watch rated R movies:

```javascript
const canWatchRatedR = moviePatrons.filter(function(patron) {
  return patron.age > 17;
});

```

In this code, `filter` is called on the `moviePatrons` array. The provided function returns a boolean value based on whether the patron's age is greater than 17. The new array `canWatchRatedR` is then created with only the `patron` objects that pass the filter function.

3.  Using `map` to create a new array with a new property based on each patron's age:

```javascript
const cardedMoviePatrons = moviePatrons.map(patron => {
  const pObj = { ...patron };
  if (pObj.age >= 17) {
    pObj.canWatchRatedR = true;
  } else {
    pObj.canWatchRatedR = false;
  }
  return pObj;
});

```

In this code, `map` is called on the `moviePatrons` array. The provided function creates a new object `pObj` for each `patron` object in the array. The `...` operator is used to copy all the properties of the `patron` object into the new object. Then, a new property `canWatchRatedR` is added to the object based on the patron's age. The new array `cardedMoviePatrons` is then created with the new objects.