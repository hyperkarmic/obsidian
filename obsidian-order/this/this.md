# this

-   In a method, `this` refers to the **owner object**.
- #### When you create an object of a function using new keyword then `this` will point to that particular object
- .  When used alone, `this` refers to the **global object**.
-   In a function, `this` refers to the **global object**.
- #### When a function includes `this` keyword and is called from the global scope then `this` will point to the window object.
- In a function, in strict mode, `this` is `undefined`.
-   In an event, `this` refers to the **element** that received the event.
-   Methods like `call()`, and `apply()` can refer `this` to **any object**.
- #### The main purpose of call() and apply() is to set the context of `this` inside a function irrespective whether that function is being called in the global scope or as object's method.
***
This keyword:Is a context object!!!!
****
## This: What is **this**?The JavaScript `this` keyword refers to the object it belongs to.
***

**This:** The `this` keyword refers to an object so that you can access the properties within an object. It can also be used to set the value of a property within an object.
***
![[TDD/this'.png]]
***
![[TDD/this2.png]]
***
![[TDD/this3.png]]
***
**This has five scenarios:**

(1) The binding event points to the event itself

(2) Ordinary function, pointing to the method body

(3) The new function points to the current class

(4) Arrow function, pointing to the parent context

(5) call/apply/bind
***

#this
