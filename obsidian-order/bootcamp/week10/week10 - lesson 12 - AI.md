This is a test-driven development exercise where you will write test cases to validate two constructor functions, Child and DayCare, and their associated methods.

The `Child` constructor expects a `name` and an `age`. If `name` is not a string or `name` is an empty string, an error is thrown. If `age` is not a number, is `NaN`, or is less than `0`, an error is thrown. Otherwise, these values are added to the created instance when the constructor is called.

The `DayCare` constructor has an empty `children` array, a capacity of 3, and an `ageLimit` of 6. It has two methods: `addChild`, which adds `Child` objects to the `children` array, and `pickupChild`, which removes a `Child` object from the `children` array.

The `index.js` file imports the `DayCare` and `Child` constructor functions, and includes Jest test cases to validate their functionality. The `child.test.js` file contains test cases for the `Child` constructor function, and the `dayCare.test.js` file contains test cases for the `DayCare` constructor and its associated methods.

The purpose of this exercise is to practice writing test cases for code and to follow the Arrange, Act, Assert pattern. The test cases will ensure that the code behaves as expected, and will catch any potential bugs or errors in the code.

***
This exercise involves testing two constructor functions, `Child` and `DayCare`. The `Child` constructor expects a `name` (string) and an `age` (number) and creates a new instance of a child. The `DayCare` constructor creates a new instance of a daycare and has an empty `children` array, a capacity of 3, and an `ageLimit` of 6. The `DayCare` constructor has two methods, `addChild`, which adds a `Child` object to the `children` array, and `pickupChild`, which removes a `Child` object from the `children` array.

The exercise requires writing tests for both constructors in `child.test.js` and `dayCare.test.js` respectively. In `child.test.js`, the tests should ensure that the `Child` constructor works as expected by testing positive, negative, and exception cases. In `dayCare.test.js`, the tests should ensure that the `DayCare` constructor and methods work as expected.

The `index.js` file contains Jest tests for the `DayCare` constructor and methods that can be run using the `npm run test` command.

To run the tests, you must have `jest` installed as a dev dependency, which is specified in the `package.json` file.

Here is an example of a test from `index.js` that tests the `addChild` method of the `DayCare` constructor:

```javascript
describe("addChild", () => {
  it("should add a child to the 'children' array", () => {
    const child = new Child("Tammy", 1);
    const dayCare = new DayCare();

    dayCare.addChild(child);

    expect(dayCare.children.length).toEqual(1);
    expect(dayCare.children[0]).toBe(child);
  });

  it("should not add a child over the 'ageLimit'", () => {
    const child = new Child("Tammy", 8);
    const dayCare = new DayCare();

    dayCare.addChild(child);

    expect(dayCare.children.length).toEqual(0);
  });

  it("should not add a child if already at capacity", () => {
    const dayCare = new DayCare();
    const child = new Child("Alice", 4);
    dayCare.children = [      new Child("Tammy", 1),      new Child("Mark", 2),      new Child("Alvin", 1)    ];

    dayCare.addChild(child);

    expect(dayCare.children.length).toEqual(3);
  });

  it("should throw an error if not provided a Child object as an argument", () => {
    const err = new Error(
      "Expected parameter 'child' to be an instance of Child"
    );
    const cb = () => {
      const dayCare = new DayCare();
      dayCare.addChild();
    };

    expect(cb).toThrowError(err);
  });
});

```

This test suite checks that the `addChild` method adds a child to the `children` array if the child's age is within the age limit and the daycare is not already at capacity. If the child's age is above the age limit, the method should not add the child to the array. If the daycare is already at capacity, the method should not add the child to the array. Finally, if the method is not provided with a `Child` object as an argument, it should throw an error.