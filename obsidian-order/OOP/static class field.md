# # **Static Class Field**

static is a keyword that we can add before a field or method, usually, when we create a field or method, the field will automatically become a property in the object instance, and the method will become a function in the prototype.  
If we add static, then it doesn’t happen.

If we add static in the class field, automatically the field no longer belongs to the object instance but belongs to the class itself

Usually, static is used if we want to create a utility field or function. How to access the static class field is no longer through the object but the class

Static class field can be interpreted as global, no matter where it is accessed or who is accessing it, the result will be the same

``` javascript
class MathUtil {  
static sum(...numbers) {  
let total = 0;  
for (const number of numbers) {  
total += number;  
}  
return total;  
}  
}
```

***
A static member of a class is one that is related at the class level rather than at the level of the object instance. At the class level, a static member has just one instance. Static functions were formerly defined by layering a method or variable on top of a function object. With ES6, JavaScript, on the other hand, gives you an approach that you’d expect in any OOP paradigm. The static keyword may now be used to designate a method as being static.
***

#static #static-field #classes #javascript 