# Class - Keyword
``` javascript
class Person {  
constructor(name) {  
    
  }  
}const name = new Person("Adi")  
console.info(name)
```
***
In the class, we can also add a constructor, whereby using the constructor, we can also add parameters when we first create the object

To create a constructor in a class, we can use the `constructor` keyword

***
# Method in Class

Creating a method in a class can be done in a way like adding a method in the constructor function

However, it adds a method to the object instance. Especially for methods, we should add to the prototype, not to the object instance

Fortunately, in the class, there is an easy way to add a method and it is automatically added to the prototype

``` javascript
class Person {  
  constructor(name) {  
    this.name = name  
  }  sayHello(name) {  
    console.info(`Hi ${name}, my name is ${this.name}`);  
  }  
}
```



***

# **What are classes in JavaScript?**

JS classes are templates for creating objects. They reduce duplicate code and debugging time. Developers use classes to produce similar objects. Like functions, classes can be used both in declaration and expression.
***
#class #keyword
