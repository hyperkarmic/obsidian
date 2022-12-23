# SOLID

## **The SOLID principles do not only apply on software development but also when architecting a system.**


## **➊ —** Single Responsibility Principle

> **_A class should have one, and only one, reason to change._**

This principle postulates that it is preferable to extend a system behaviour, without modifying it.

## **➋ —** Open-Closed Principle

> **_You should be able to extend a class’ behaviour, without modifying it._**

The classes you use should be open for extension but closed for modification. One way to achieve this is via inheritance i.e. create a sub-class so the original class is closed for modification, but custom code is added to the sub-class to introduce a new behaviour.

## **➌ —** Liskov Substitution Principle

> **_Derived classes must be substitutable for their base classes._**

When extending the behaviour of a class A into a sub-class B you must ensure that you can still exchange A with B without breaking anything. This can be a bit catchy especially when combining this principle with the Open-Closed one.

In Software Development, this means that derived classes must be substitutable for their base classes,

## **➍ —** Interface Segregation Principle

> **_Make fine grained interfaces that are client specific._**

Interfaces and classes must be as specialised as possible, so calling clients do not depend on methods they don’t use. This goes hand in hand with the Single Responsibility principle.

Interfaces/contracts must be as fine grained as possible and client specific, so calling clients do not depend on functionality they don’t use.

## **➎ —** Dependency Inversion Principle

> **_Depend on abstractions, not on concretions._**

High level classes should not depend on low level ones. They should both depend on abstractions. Likewise, abstractions should not depend on details. Details should depend on abstractions.

High level modules should not depend on low level ones; they should both depend on abstractions. Likewise, abstractions should not depend on details, but details should depend on abstractions.
***
The **SOLID Principles** were presented initially by Uncle Bob in his book **Agile Software Development: Principles, Patterns, and Practices** and they intended to make software designs more understandable, flexible and maintainable.
***
According to Uncle Bob, they are:

> The SOLID principles are not rules. They are not laws. They are not perfect truths. The are statements on the order of _“An apple a day keeps the doctor away.”_ This is a good principle, it is good advice, but it’s not a pure truth, nor is it a rule.
> 
> The principles are mental cubby-holes. They give a name to a concept so that you can talk and reason about that concept. They provide a place to hang the _feelings_ we have about good and bad code. They attempt to categorize those feelings into concrete advice. In that sense, the principles are a kind of anodyne. Given some code or design that you _feel bad_ about, you may be able to find a principle that explains that bad feeling and advises you about how to feel better.
> 
> These principles are heuristics. They are common-sense solutions to common problems. They are common-sense disciplines that can help you stay out of trouble. But like any heuristic, they are empirical in nature. They have been observed to work in many cases; but there is no proof that they always work, nor any proof that they should always be followed.
> 
> [**Getting a SOLID start**](https://sites.google.com/site/unclebobconsultingllc/getting-a-solid-start) **by Uncle Bob**

***


Let’s analyse them with practical examples in javascript

# **Single Responsibility Principle (SRP)**

> _A class should have one, and only one, reason to change._

The idea behind this principle is we need to split different responsibilities into different classes, we have the following code below that illustrates the User class:

The problem with this example is the User class has to manage two different responsibilities:

-   Edit user data
-   Logs the user data edition

This generates problems to maintain stability, once we have more than one reason to change this class, let’s suppose that we need to implement a better Log control with date and time, when we add this we could break things that’s is not directly with Log like edit user name or age, also, this will become this class bigger than it needs to be.

We could recreate this code using the Proxy Pattern, and the result will be:

Now we have two classes with different responsibilities:

-   **User class:** Manages only stuffs related directly to user data (edit name and age)
-   **UserLogProxy:** Manage only the logs of user actions

# Open/Closed Principle (OCP)

> _Objects or entities should be open for extension, but closed for modification._

There is only one constant in code development which is **C H A N G E S**, everything that we code will change at some moment in future, so we need to create code that makes it easier.

**The way that we change our code will define the code quality**, if we constantly change our current classes, this will generate bugs in our code, but if we extend our classes with new ones this will help us to avoid bugs in our code, that’s the main idea of **OCP Principle**.

Let’s analyse the code below:

If we want to add a new Sandwich size, giant, for example, we need to edit the Sandwich class, and potentially break something else, if we delegate this list to another class and load this class from the Sandwich class we make the future manutention easier and safer:

Now we have 2 different classes connected through the setSize method in the Sandwich class, it doesn’t matter how many sizes we’d like to add we don’t need to edit the Sandwich class anymore, that’s the OCP Principle essence.

# Liskov substitution principle

> _Let q(x) be a property provable about objects of x of type T. Then q(y) should be provable for objects y of type S where S is a subtype of T._

This definition doesn’t help us to understand faster what’s this principle means, but the idea is very simple: **a parent class could be replaced by a derived class without breaking its behaviour**.

The code below is a classic example of a derived class breaking the behaviour of a parent class:

The problem in this example is the derived class Square changes how is calculated the area of his parent class Rectangle, **this is a classic case where a Duck that needs batteries don’t replace a real Duck,** in our example if Square can’t replace a Rectangle its means that Square shouldn’t inherit from Rectangle class.

![](https://miro.medium.com/max/640/0*FdopVquiGKzUEIEX.jpg)

Found [here](https://lostechies.com/derickbailey/2009/02/11/solid-development-principles-in-motivational-pictures/)

To solve this, we could reimplement this algorithm using this approach:

Now the Rectangle class and Square class are independent classes, avoiding the Square class changes the Rectangle class's behaviour.

# **Interface Segregation Principle (ISP)**

> _Clients should not be forced to depend upon interfaces that they do not use._

You could think “Ok there is no problem here once Javascript doesn’t provide Interfaces types”, but we could use this principle to avoid sending useless parameters like in the example below:

In this example the method setName in the Product class always requires the user to send the onFinish function even when the user doesn’t need to call this function, this is better implemented in this way:

The change between the two codes is subtle but greatly improves the implementation of the code, instead of this:

setName({ _name_, **_onFinish_** }) {  
  _this_.name = name;  
  onFinish(_this_);  
}

We put this:

setName({ _name_, **_onFinish = () => {}_** }) {  
  _this_.name = name;  
  onFinish(_this_);  
}

We are using the **Object Destructuring** ES6 feature to create a clean code! If you want to know more about Destructuring, I wrote an article about this:

[

## #8 Functional Approach: Destructuring

### When we call a JS function we have problems identifying the parameters name, once we only send the argument, like in…

medium.com



](https://medium.com/@_rxluz/8-functional-approach-destructuring-b39dcbb40683)

# Dependency Inversion Principle (DIP)

> 1. High-level modules should not depend on low-level modules. Both should depend on abstractions.
> 
> 2. Abstractions should not depend upon details. Details should depend upon abstractions.

The idea here is to create a way to become our classes less dependent on other classes, making it easier to replace dependency on others.

To visualize this in a real situation let’s analyse the code below:

In this example, we have the Client class tightly coupled with ValidateEmailSimple, every time that we call the setEmail we create a new instance from ValidateEmailSimple, the problem here is when you decide to change this validation to another more complex (ValidateEmailAdvanced), you’ll need a change in Client class all occurrences to the old Validation system, and this could create new bugs and inconsistency in our application.

The solution to solve this transforms this **tightly coupled dependency** into a **loosely coupled dependenc**y, how to do that? Simple, let’s create a var inside our Client class called _emailValidationService, and call this to validate our email instead of calling directly the validation Class that we need:

With this approach, we don’t need to change the Client class when we decide to put a more advanced Validation Email System, cool right?

If you want to know more about **Design Patterns** and **SOLID Design Principles** I recommend these books:

-   **Design Patterns: Elements of Reusable Object-Oriented Software by GoF**
-   **Agile Principles, Patterns, and Practices in C# by Micah Martin and Robert Cecil Martin**
-   **Head First Design Patterns by Elisabeth Freeman and Kathy Sierra**
-   **Learning JavaScript Design Patterns by Addy Osmani**

***
![[solid.png]]
***
![[solid2.png]]
***
![[single-responsibility.png]]
***

![[open-closed.png]]
***
![[liskov-corona.png]]
***
![[interface-segregation-principle.png]]
***
![[dependency-inversion.png]]