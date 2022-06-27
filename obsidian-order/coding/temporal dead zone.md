# temporal dead zone
**he temporal dead zone** is the phase between _hoisting_ and where that variable is assigned with a value. A _let_ or _const_ variable cannot be accessed when it is in the temporal dead zone. It will give a _reference error_. And another important aspect is that a _let_ or _const_ variable cannot be redeclared like _var_. In such a situation, a _syntax error_ will be given. But what is the difference between _let_ and _const_? The _let_ can be declared and initialized at any point in the program. But _const_ can only be declared and initialized in the same line. The value of _const_ cannot be updated later in the code.

#hoisting
#temporal-dead-zone
#js #javascript #coding 