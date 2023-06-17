## What exactly is dependency injection?

Dependency Injection (DI) is a design pattern in software development that makes it easier to manage the relationships between different components or objects in a program.

In simple terms, it’s a way to provide the necessary dependencies (services, objects, or values) to a component from an external source rather than having the component create or find them on its own.

Imagine you’re building a toy car, and instead of having each part (like wheels, body, and engine) find or create its screws, you provide them from the outside. This makes it easier to change the screws or reuse the parts in different combinations without changing the parts themselves.

## What are the advantages of dependency injection?

Dependency Injection helps with the following:

1.  Flexibility: It makes it easier to change or swap dependencies without modifying the components that use them.
2.  Reusability: Components become more reusable because they’re not tightly coupled to specific dependencies.
3.  Testability: It’s easier to test components by providing mock dependencies during testing.

## What types of dependency injection are there?

There are three common ways to implement Dependency Injection. We will outline each approach and provide an example for each. Before diving into the examples, let’s look at a `Car` class implementation without dependency injection.

```python
class Car:  
    def __init__(self):  
        self.engine = Engine()  
  
    def start(self):  
        return self.engine.start()
```

In this implementation, the `Car` class creates an `Engine` object in its constructor, resulting in tight coupling between the classes. Now, let's explore the three dependency injection techniques along with examples to improve this code.

1.  **Constructor Injection**: In this approach, the dependencies of a class are supplied through its constructor. In the example below, the `Car` class depends on the Engine class. By using constructor injection, the `Car` class receives an instance of the `Engine` as a constructor argument, thus eliminating the need for the `Car` class to create the `Engine` instance itself. This way, the `Car` class remains dependent on the `Engine` class but no longer has the responsibility of instantiating it.

```python
class Car:  
    def __init__(self, engine):  
        self.engine = engine  
  
    def start(self):  
        return self.engine.start()
```

**2. Setter Injection**: The setter methods in the class provide the dependencies. In the example below, the dependency of the Car, the engine is injected via the `set_engine` method.

```python
class Car:  
    def __init__(self):  
        self.engine = None  
  
    def set_engine(self, engine):  
        self.engine = engine
```
3. **Method Parameter Injection**: The dependencies are provided as parameters to the methods that use them. In the example below, the dependency of the car, the engine, is injected through the `start` method.

```python
class Car:  
    def start(self, engine):  
        return engine.start()
```

Each approach has its advantages and use cases. Constructor and setter injections are the most commonly used, as they balance flexibility and simplicity.