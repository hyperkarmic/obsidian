# react hooks - Positives
-   Improved code reuse;
-   Better code composition;
-   Better defaults;
-   Sharing non-visual logic with the use of custom hooks;
-   Flexibility in moving up and down the `components` tree.

-   **Reusing stateful logic between components is difficult.**  
    With Hooks, you can reuse logic between your components without changing their architecture or structure.
-   **Complex components can be difficult to understand.**  
    When components become larger and carry out many operations, it becomes difficult to understand in the long run. Hooks solve this by allowing you separate a particular single component into various smaller functions based upon what pieces of this separated component are related (such as setting up a subscription or fetching data), rather than having to force a split based on lifecycle methods.
-   **Classes are quite confusing.**  
    Classes are a hindrance to learning React properly; you would need to understand how `this` in JavaScript works which differs from other languages. React Hooks solves this problem by allowing developers to use the best of React features without having to use classes.
<hr>
### They were introduced at the [React Conf 2018](https://www.youtube.com/watch?v=dpw9EHDh2bM) to address three major problems of class components: wrapper hell, huge components, and confusing classes. Hooks give power to React functional components, making it possible to develop an entire application with it.
<hr>
### WRAPPER HELL 

Complex applications built with class components easily run into wrapper hell. If you examine the application in the React Dev Tools, you will notice deeply nested components. This makes it very difficult to work with the components or debug them. While these problems could be solved with **higher-order components** and **render props**, they require you to modify your code a bit. This could lead to confusion in a complex application.
<hr>
### HUGE COMPONENTS 

Class components usually contain side effects and stateful logic. As the application grows in complexity, it is common for the component to become messy and confusing. This is because the side effects are expected to be organized by **lifecycle methods** rather than functionality. While it is possible to split the components and make them simpler, this often introduces a higher level of abstraction.

Hooks organize side effects by functionality and it is possible to split a component into pieces based on the functionality.

<hr>
<hr>
### CONFUSING CLASSES 

Classes are generally a more difficult concept than functions. React class-based components are verbose and a bit difficult for beginners. If you are new to Javascript, you could find functions easier to get started with because of their lightweight syntax as compared to classes. The syntax could be confusing; sometimes, it is possible to forget binding an event handler which could break the code.

<hr>
here’s a few solid reasons to use functional components instead of classes, and utilize hooks:

-   less boilerplate code (no need for constructors, state, etc)
-   increased optimization
-   no need to change your functional components to manage state
<hr>
Some benefits are

-   Isolating stateful logic, making it easier to test.
-   Sharing stateful logic without render props or higher-order components.
-   Separating your app’s concerns based on logic, not lifecycle hooks.
-   Avoiding ES6 classes, because they’re quirky, _not actually classes,_ and trip up even experienced JavaScript developers.
<hr>
The primary purpose of using the **Class Component** was to obtain access to the state and the life cycle methods, which were unavailable in the **Functional Components**. **Hooks** allows the use of these features in the **Functional Components** , without using the less performant **Class Component** counterparts.
<hr>


#react #hooks #positives