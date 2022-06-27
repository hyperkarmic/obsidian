# instanceOf

The instanceof operator supports class inheritance, meaning that instanceof can also be used to check whether an object is an instance of a certain class or an instance of a certain class?

``` javascript
class Employee {}class Manager extends Employee {}const budi = new Employee();  
const adi = new Manager();console.info(budi instanceof Employee); // true  
console.info(budi instanceof Manager); // false_// true because Manager is an inheritance from the Employee_  
console.info(adi instanceof Employee); // true  
console.info(adi instanceof Manager); // true
```
#instanceOf  
#js #javascript #OOP 


static is a keyword that we can add before a field or method, usually, when we create a field or method, the field will automatically become a property in the object instance, and the method will become a function in the prototype.  
If we add static, then it doesn’t happen.

If we add static in the class field, automatically the field no longer belongs to the object instance but belongs to the class itself

Usually, static is used if we want to create a utility field or function. How to access the static class field is no longer through the object but the class

Static class field can be interpreted as global, no matter where it is accessed or who is accessing it, the result will be the same