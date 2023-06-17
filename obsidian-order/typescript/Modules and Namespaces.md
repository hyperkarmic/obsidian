### Modules and Namespaces

TypeScript has built-in support for modules and namespaces. Modules allow you to organize your code into reusable, shareable units. For example, we can define a `Greeter` class in a separate file `greeter.ts` and then import it into our main file `app.ts` like this:

```typescript
// greeter.ts <- FileName
export class Greeter {
  // ...
}

// app.ts <- FileName
import { Greeter } from './greeter';

let greeter = new Greeter('TypeScript');
greeter.greet();

```

Namespaces allow you to group related code. For example, we can define a namespace `MyNamespace` that has a `message` property.

```typescript
namespace MyNamespace {
  export const message = 'Hello, TypeScript!';
}

console.log(MyNamespace.message);

```

***
Namespaces in TypeScript are a way to organize and group related code. They help you avoid naming collisions and promote modularity by encapsulating code that belongs together. Namespaces can contain classes, interfaces, functions, variables, and other namespaces.

## Defining Namespaces

To define a namespace, use the `namespace` keyword followed by the namespace name. You can then add any related code inside the curly braces.

```typescript
namespace MyNamespace {  
  export class MyClass {  
    constructor(public value: number) {}  
  
    displayValue() {  
      console.log(`The value is: ${this.value}`);  
    }  
  }  
}
```

In this example, we define a namespace called `MyNamespace` and add a class `MyClass` inside it. Notice that we use the `export` keyword to make the class accessible outside the namespace.