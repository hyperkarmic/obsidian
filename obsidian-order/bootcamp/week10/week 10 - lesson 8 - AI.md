This is an exercise that demonstrates how to use Test Driven Development (TDD) to write code. The code is written in JavaScript and includes three files, `index.js`, `arithmetic.js`, and `arithmetic.test.js`. `arithmetic.js` contains a class named `Arithmetic`, which has methods for addition, subtraction, and a `value()` method that returns the current value of the object. `index.js` is used to test the `Arithmetic` class using method chaining. Finally, `arithmetic.test.js` is used to run tests on the `Arithmetic` class to verify that it functions as expected.

Learning Outcomes:

-   Understand the concept of TDD and how it can be applied to writing code
-   Learn how to write and run tests using Jest
-   Learn how to create and use classes and objects in JavaScript
-   Understand the concept of method chaining in JavaScript

Code Explanation:

1.  `index.js`: This file contains code that creates an instance of the `Arithmetic` class and uses method chaining to perform arithmetic operations on it. Finally, it logs the value of the object to the console.

```javascript
const Arithmetic = require("./arithmetic");

const value = new Arithmetic(4)
  .plus(8)
  .plus(15)
  .minus(16)
  .minus(23)
  .plus(42)
  .plus(108)
  .value();

console.log(value);

```

2.  `arithmetic.js`: This file contains the `Arithmetic` class definition. The class has methods for addition, subtraction, and a `value()` method that returns the current value of the object.

```javascript
function Arithmetic(number = 0) {
  this.number = number;
}

Arithmetic.prototype.plus = function(num = 0) {
  const newNumber = this.number + num;

  return new Arithmetic(newNumber);
};

Arithmetic.prototype.minus = function(num = 0) {
  const newNumber = this.number - num;

  return new Arithmetic(newNumber);
};

Arithmetic.prototype.value = function() {
  return this.number;
};

module.exports = Arithmetic;

```

3.  `arithmetic.test.js`: This file contains tests for the `Arithmetic` class. The tests are written using Jest, which is a testing library for JavaScript. The tests are grouped into different `describe` blocks, each focusing on a specific method of the `Arithmetic` class. The tests check if the methods return the expected output.

```javascript
const Arithmetic = require("../arithmetic");

describe("Arithmetic", () => {
  describe("Initialization", () => {
    it("should return an object containing a 'number' property when called with the 'new' keyword", () => {
      const obj = new Arithmetic();

      expect("number" in obj).toEqual(true);
    });

    it("should set 'number' when created", () => {
      const num = 108;

      const obj = new Arithmetic(num);

      expect(obj.number).toEqual(num);
    });

    it("should default 'number' to 0", () => {
      const obj = new Arithmetic();

      expect(obj.number).toEqual(0);
    });
  });

  describe("plus", () => {
    it("should return a new 'Arithmetic' object", () => {
      const obj = new Arithmetic(3).plus(3);

      expect(obj instanceof Arithmetic).toEqual(true);
    });

    it("should return a new 'Arithmetic' object that has an updated 'number' value", () => {
      const num = 8;
      const added = 7;
      const sum = num + added;

      const { number } = new Arithmetic(num).plus(added);


```
