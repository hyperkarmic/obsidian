Functions in TypeScript can have types for their parameters and return values. For example, we can define a function `addNumbers` that takes two `number` parameters and returns a `number`:

```typescript

function addNumbers(a: number, b: number): number {  //here `number` is the type of `a` and `b`. It means, we can also assign numbers to them, if we will try to give any other values like string or boolean, then it will going to give us error. 
  return a + b;
}

```

