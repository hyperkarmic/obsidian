# constructor inheritance
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
