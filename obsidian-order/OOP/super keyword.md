# super keyword
The super keyword is used to call the `super` class constructor. If in the child class we create a constructor, then we must call the parent constructor, even though there is no constructor in the parent
***
Besides being used to call the parent class’s constructor, `super` keyword can also be used to access parent class methods. You can do this by using the super point of the function name

In other words, super is a reference to the parent prototype, much like `__proto__`
***
To call the constructor of the parent class, the derived class expects you to use the super keyword. This makes sense because you don’t want to duplicate the parent class’s initiation logic in the derived class.
***
If you don’t explicitly specify a _constructor_ in the derived class, JavaScript creates one for you and calls the _super_ keyword, which launches the parent class’s constructor method. If a derived constructor is explicitly defined, it must call the parent constructor by explicitly invoking _super_ in the derived class before accessing this or returning from a derived constructor. Because the super call, even within the constructor, will create the _this_ object, it is critical that you call super before using this to initialize any other member variable.
***

#super
#keyword
