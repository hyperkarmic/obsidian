![[creation-phase.jpeg]]
***
![[eq-creation-phase.jpg]]
***
![[execution-context-creation-phase.jpg]]

![[creation-phase.jpg]]

![[creation-phase2.jpg]]
***
## creation phase

1.  **Creation of an execution context**: A new execution context is created for the code being executed. Each time a script or function is invoked, a new execution context is created. This context contains information about the current scope, variable environment, and the value of `this`.
2.  **Hoisting**: Variable and function declarations are processed and moved to the top of their respective scopes. Variables declared with `var` are initialized with the value `undefined`. This means that variable declarations are processed before any code is executed, and they are accessible to the entire scope, even before they are defined in the code.
3.  **Creation of the variable environment**: The variable environment is created, which includes the variable and function declarations that are accessible within the current execution context. This environment holds the values of all variables and functions defined in the current scope.

The creation phase is an important concept to understand when working with JavaScript, as it affects the way variable and function declarations are processed and can affect the behavior of your code. Understanding the creation phase and how it works can help you write better and more efficient JavaScript.

***

#execution-context #creation #creation-phase #phases 