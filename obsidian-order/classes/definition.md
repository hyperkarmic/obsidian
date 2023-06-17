# classes

_Class:__In object-oriented programming, a class defines a structure for creating objects consisting of variables or attributes and functions or methods._

Each of these objects is then called an “instance” of the class.
<hr>
_Class:_ _In object-oriented programming, a_ _class_ _is an extensible program-code-template for creating objects, providing initial values for state (member variables) and implementations of behavior (member functions or methods)._
<hr>
_Class:__"a class in a program is a definition of a “type” of custom data structure that includes both data and behaviors that operate on that data. Classes define how such a data structure works, but classes are not themselves concrete values. To get a concrete value that you can use in the program, a class must be instantiated (with the "new" keyword) one or more times."_
<hr>
_Class:_ _Classes define objects that share certain properties. Classes can be thought of as types_
<hr>
Class:Class in JavaScript serves the same purpose as in any OOP language, i.e to create a blueprint for objects.
***
Classes Unlike the classes in Object-Oriented Mode, JavaScript classes are just special type of functions. But instead of using the "function" keyword we use the "class". It was introduced in JavaScript to make the syntax look like other object-oriented languages (java, python, c++).
<hr>

Class is a blueprint, prototype, or template for creating an Object. Class contains declarations of all properties and functions that are owned by the Object
***


Every object is always created in Class. And a class can create an unlimited object
***
![[class-def.jpg]]
***
# Class and Object

-   Object is a thing which can be seen or touched and in software we try to represent the same real-life thing with object.
-   Object Oriented Programing is nothing but code around that object.
-   Class is not an object, it’s like blueprint which can generate objects. So, class helps to set the classification of objects with its properties and capabilities.
-   Any number of instance can be created from a class, each instance is called Object.
***
a js class example

```javascript
class Person { constructor(name, age) { this.name = name; this.age = age; } greet() { console.log(`Hello, my name is ${this.name}, and I am ${this.age} years old.`); } } const john = new Person('John', 25); john.greet(); // Output: Hello, my name is John, and I am 25 years old.
```

another one

```javascript
class Employee extends Person { constructor(name, age, title) { super(name, age); this.title = title; } work() { console.log(`${this.name} is working as a ${this.title}.`); } } const alice = new Employee('Alice', 30, 'Software Developer'); alice.greet(); // Output: Hello, my name is Alice, and I am 30 years old. alice.work(); // Output: Alice is working as a Software Developer.
```

#classes #class #OOP 