# inheritance

(1) Prototype chain inheritance: overrides the object.

It has two disadvantages: 1) object instances share all inherited properties and methods. 2) Cannot pass parameters

(2) Constructor inheritance: call the supertype constructor inside the subclass constructor. Use the apply () and call () methods

Its disadvantages are: (a) function reusability is not high. Every instance is a re-instantiated constructor, and there is no shared attribute. (b) it can only inherit the attribute on the instance, and the method on the prototype is invisible.

(3) Composite inheritance: prototype chain + constructor parent Call (this) new parent() avoids the above shortcomings.

Advantages: it can pass parameters and will not be shared with the parent class reference attribute

Disadvantages: when inheriting the function of the parent class, the constructor of the parent class is called, resulting in unnecessary parent class attributes on the prototype of the child class, which is a waste of memory.

(4) Prototype inheritance: the object () function performs a shallow copy of the object passed in

(5) Parasitic inheritance: use constructors to inherit attributes, and inherit methods through the hybrid form of prototype chains

(6) Parasitic composition only calls the constructor once, which combines the advantages of parasitic inheritance and composite inheritance. It is the most effective way to realize type-based inheritance. It is to assign the prototype of the parent class to the child class and set the constructor as the child class, which solves the useless parent attribute problem, parent call + Object.create(）
***
![[inheritance-oop.jpg]]
***
Inheritance in most class-based object-oriented languages is a mechanism in which one object acquires all the properties and behaviors of another object.
***
## Prototypal Inheritance (Behavior delegation pattern)

-   `v1` and `v2` are linked to `Vehicle.prototype` because it’s been created using _new_ keyword.
-   Similarly, `c1` and `c2` is linked to `Car.prototype` and `Car.prototype` is linked to `Vehicle.prototype`.
-   In JavaScript when we create the object it does not copy the properties or behavior, it creates a link. Similar kind of linkage gets created in case of extend of class as well.
-   All arrows go in the opposite direction compare to classical non-js inheritance because it’s a behavior delegation link. These links are known as prototype chain.
-   This pattern is called _Behavior Delegation Pattern_ which commonly known as **_prototypal inheritance_** in JavaScript.
***

#inheritance #OOP