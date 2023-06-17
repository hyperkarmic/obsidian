TypeScript also supports classes and objects. We can define a class `Greeter` that has a `greeting` property and a `greet` method:

```typescript
class Greeter {
  greeting: string;

  constructor(message: string) {
    this.greeting = message;
  }

  greet() {  //this is greet method/function
    console.log(`Hello, ${this.greeting}!`);
  }
}

```

We can then create an object of the type `Greeter` and call its `greet` method:

```typescript
let greeter = new Greeter('TypeScript');
greeter.greet(); // Hello, TypeScript!

```

