This project contains a small program which simulates a daycare facility with the ability to add children to the daycare, pick them up and throw errors if necessary. This activity requires the students to write tests to verify the proper functioning of the program with Jest. The program also uses Jest's built-in mock implementation to spy on console.log() to ensure that it was called as expected and with the correct arguments. The program is divided into three main files: `index.js`, `child.js`, and `dayCare.js`.

The program uses classes to represent a child and a daycare, which are located in the `child.js` and `dayCare.js` files, respectively. The `child.js` file contains the `Child` class, which has two properties, `name` and `age`. The `dayCare.js` file contains the `DayCare` class, which has three properties, `children`, `capacity`, and `ageLimit`, as well as three methods, `addChild`, `pickupChild`, and `printChildList`.

The `index.js` file is the entry point for the program and tests the `DayCare` class's various methods. It includes several test cases for the `addChild`, `pickupChild`, and `printChildList` methods.

The `package.json` file includes the necessary dependencies for the project, which include Jest.

The `test` directory includes two Jest test files, `child.test.js` and `dayCare.test.js`. The `child.test.js` file includes test cases for the `Child` class, and the `dayCare.test.js` file includes test cases for the `DayCare` class. These tests are meant to ensure that the various methods of these classes are working correctly.

The key learning outcomes for this project include writing tests for code, testing classes, and working with Jest to spy on console.log(). By testing classes, students will learn how to write unit tests that focus on a specific part of the code. By writing tests for console.log(), students will learn how to use Jest's mock implementation to verify that specific methods were called with the correct arguments.
***
This code exercise is designed to teach developers how to use Jest mocking library to test JavaScript code that has console.log statements.

The code is written in JavaScript and consists of four files; a README file, a package.json file, an index.js file, and a child.js file. Additionally, there are two jest test files located in a sub-folder called “test”.

The index.js file exports an instance of the DayCare class and requires the Child class defined in the child.js file. The code exports a module with several methods:

1.  Initialization: A function that creates a new object with children, capacity, and ageLimit properties.
    
2.  addChild: A function that adds a child object to the array of children only if the following conditions are met: the age is less than the age limit, and there is room in the daycare. Otherwise, an appropriate message is logged to the console.
    
3.  pickupChild: A function that removes a child object from the array of children by searching for the first child with a matching name property. If no child with a matching name is found, an appropriate message is logged to the console.
    

The child.js file exports a Child class, which takes two arguments; name and age. If name is not a string or is an empty string, an error is thrown.

The test folder contains two Jest test files.

**Test File 1:** This test file imports the DayCare and Child classes and tests the following methods in the DayCare class:

1.  Initialization: Tests whether a new object is created with expected properties.
2.  addChild: Tests whether the child object is added to the array of children if the child's age is less than the age limit and there is room in the daycare. The test also checks if an appropriate message is logged to the console if the child is too old, if there is no room in the daycare, or if an argument is not provided.
3.  pickupChild: Tests whether a child object is removed from the array of children by searching for the first child with a matching name property. The test also checks whether an appropriate message is logged to the console if no child with a matching name is found.

**Test File 2:** This test file uses the jest library to mock the console.log method and tests whether the expected console.log statements are called with the correct arguments in the DayCare class. This is done by testing whether the mocked console.log method is called with the expected arguments when the addChild method is called with various inputs.

**Key code snippets:**

1.  Adding a child object to the array of children only if the following conditions are met: the age is less than the age limit, and there is room in the daycare.

```javascript
  addChild(child) {
    if (!(child instanceof Child)) {
      throw new Error("Expected parameter 'child' to be an instance of Child");
    }

    if (child.age > this.ageLimit) {
      console.log("Unable to add child, they are over the age limit");
    } else if (this.children.length >= this.capacity) {
      console.log("At capacity, unable to add more children");
    } else {
      this.children.push(child);
    }
  }

```

2.  Removing a child object from the array of children by searching for the first child with a matching name property. If no child with a matching name is found, an appropriate message is logged to the console.

```javascript
  pickupChild(name) {
    const childIndex = this.children.findIndex(child => child.name === name);

    if (childIndex === -1) {
      console.log("Child not found");
      return;
    }

    const [child] = this.children.splice(childIndex, 1);
    console.log(`Picked up ${name} from day care

```
