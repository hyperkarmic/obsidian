# how prototype inheritance works

How can the properties in the prototype be accessed from the object instance?

When we access a property in an object instance, it will first check whether the object contains the property or not, if not, it will be checked on its `__proto__` (prototype), if it still doesn’t exist, it will be checked again on `__proto__` (prototype) higher, and so on, until it ends up in the Object Prototype

#prototype #inheritance #OOP #js #javascript 