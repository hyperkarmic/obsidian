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

#SOLID
#OOP 