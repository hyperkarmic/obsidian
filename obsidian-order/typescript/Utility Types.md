Utility types in TypeScript provide a convenient way to transform existing types into new types. They allow you to create more complex and flexible types without having to define them from scratch, promoting code reusability and type safety.

## Using Utility Types

To use a utility type, apply the utility type to an existing type using the angle bracket syntax. TypeScript provides a variety of built-in utility types, such as `Partial`, `Readonly`, `Pick`, and `Omit`.

```typescript
interface Person {  
  name: string;  
  age: number;  
  email: string;  
}  
  
type PartialPerson = Partial<Person>;  
type ReadonlyPerson = Readonly<Person>;  
type NameAndAge = Pick<Person, "name" | "age">;  
type WithoutEmail = Omit<Person, "email">;
```

In this example, we define an interface called `Person` with three properties: `name`, `age`, and `email`. We then use various built-in utility types to create new types based on the `Person` interface.