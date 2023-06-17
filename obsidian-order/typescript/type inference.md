**Type inference** in TypeScript allows the compiler to infer types depending on the context. For example, if we don't specify the type parameter of the `identity` function, TypeScript will infer it based on the type of the argument:

```typescript
let result = identity('Hello, TypeScript!'); //if we'll use booleans here, then, TS will think the result is a boolean value.

```

Here, TypeScript infers that the type parameter `T` is `string` based on the argument "Hello, TypeScript!".