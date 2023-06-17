# getters and setters
**Get:** The `get` keyword will bind an object property to a function. When this property is looked up now the getter function is called. The return value of the getter function determines which property is returned.

**Set:** The `set` syntax binds an object property to a function to be called when there is an attempt to set that property.
***
# **Setter and Getter Methods**

Class method and getter syntax are the same as it is for objects except for the fact that they do not include commas between methods. We use the _get_ and _set_ keywords to define javaScript’s getters and setters for a class.

```                                javascript
class Quadrilateral {constructor(side1, side2, side3, side4) {this.side1 = side1;this.side2 = side2;this.side3 = side3;this.side4 = side4;  }  
//setters
set side1(side1){ return this.side1 = side1;  }
get side1() {return this.side1 = side1;  }}
```
***
-   The _set_ keyword binds an object property to a method that will be invoked when that property is assigned.
-   The _get_ keyword binds an object property to a method that will be invoked when that property is looked up.
***
![[why-getters&setters.jpg]]
***

#getter
#setter
#classes #es6
#javascript #JS #OOP 