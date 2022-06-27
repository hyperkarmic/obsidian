# constructor function
 

## Creating Object

We have learned the object data type, by creating a variable with the object data type

However, creating an object using the object data type, will create an object that is always unique, whereas in OOP, usually, we will create a class as a template, so that we can create objects with the same characteristics over and over again, without having to declare the object many times like using a data type object

``` js
function Person(firstName, lastName) {  
this.firstName = firstName;  
**this.lastName = lastName;  
**this.sayHello = function (name) {  
console.info(`Hello ${name}, my name is ${this.firstName}`);  
}  
}
```

***
Every time we create a constructor function, a prototype will automatically be created, for example when we create a constructor function Person, there will be a `Person.prototype`
***
When we create an object instance, the object is automatically an instance of its `Constructor.prototype`. To access prototype select an instance, we can use `__proto__` or `[[Prototype]]`
***
### Constructor functions

Functions are also objects in JavaScript. This is because just like objects, they have their own properties and methods. Functions can be used to construct objects as well, and these types of functions are known as **constructor functions**.

Constructor functions essentially eliminate the need to create separate object literals for similar tasks. They are useful because you’ll often come across situations in which you don’t know how many objects you will be creating; constructors provide the means to create as many objects as you need in an effective way.
***
