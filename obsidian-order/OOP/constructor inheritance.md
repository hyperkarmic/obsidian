
To call another constructor, we can use `NameConstructor.call(this, parameter)`

#constructor
#inheritance
#call 

``` javascript
function Employee(firstName) {

this.firstName = firstName;

this.sayHello = function (name) {

console.info(`Hi ${name}, my name is ${this.firstName}`)

}

}

function Manager(firstName, lastName) {

Employee.call(this, firstName)

this.lastName = lastName;

}
```
***
# **Constructor, Properties and Methods**

-   Constructor is just a function which gets called automatically when we create an instance from the class.
-   Instance variables get created and initialized using constructor.
-   Instance variables are nothing but called properties of the object.
-   Methods are again functions which attached with instance and all instance created from the same class will have those methods or actions.
-   Accessing properties and methods inside class, we need **_this_** keyword.
***
#constructor