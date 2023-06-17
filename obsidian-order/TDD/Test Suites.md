In Jest, a test suite is defined using the `describe` function, which takes two arguments: a string describing the suite and a callback function that contains one or more test cases using the `test` or `it` functions. The `describe` function allows for the grouping of related tests into a single suite. For example:

```javascript
describe('calculator', () => {  
  test('addition', () => {  
    expect(1+1).toBe(2);  
  });  
  
  test('subtract', () => {  
    expect(5-3).toBe(2);  
  });  
});
```

Organizing tests into suites allows you to group related tests together, which makes it easier to understand the purpose and scope of each test file. It also helps keep the test code organized and maintainable, especially as the codebase grows. Additionally, test suites can provide more granular information about the tests being run, making the test report more readable and valuable.