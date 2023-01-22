# Components


React components are basically objects that allow developers to split the traditional user interface into multiple, independent, reusable modules.

React components are divided into two types: class and function components.

**Class components** are the classic way of using components in React and they consist of extending the `React.Component` class. Although class based components are the norm during the early years of React, they are now being replaced by the newer functional component.

**Functional components** are the new way of using components in React. They are basically functions that return JSX.

Note that functional components are essentially stateless components, meaning they do not adhere to the React component lifecycle. Therefore, it is not possible to define constructors in functional components.
***
React components have a number of advantages over traditional HTML markup, some of these reasons include:

-   **Easier to scale**: Let’s assume we need to include one hundred `<a>` tags, each with a different id onto an HTML page. Using static HTML would entail having to create each one of those `<a>` tags manually, a very time consuming process. If we choose to use React components we can easily render not just `<a>` tags but an entire component that can act as an `<a>` tag, using the JavaScript `map()`

-   **Easier to update**: Let’s say you need to make a change in a `<li>` tag that is present in multiple sections of the webpage. If you're using static HTML you will have to manually find and update every single `<li>` that is present in the page. If you're using React on the other hand, assuming the `<li>` tag is contained within a component, you just need to change that single `<li>` tag and the other instances of that component will be automatically updated throughout the webpage

-   **Allows for state management**: React components allow for state management with its use of state and props(more on this below). This allows React components to automatically render its elements every time there is a state change, without any explicit action needed by the user. Plain HTML and JavaScript in comparison do not even have a concept of state management, much less implementation. React is the clear winner here.
***
Components permits to split UI into dependent reusable pieces . Serve same purpose as JavaScript function return HTML via a render function().
***
## React Component Rules:

-   Must return JSX(JS +XML)
-   take only one argument call props
-   Function name must start with Capital Letter
-   Import React from “react” [it import the react library and turn JSX we write into React.createElement()]
***
If you work with React or React Native, feel that your coding speed is slow, spend your time catching bugs, and not adding new features, work with long source files and have a hard time finding stuff, and implement the same logic over and over again, you will double your coding speed if you refactor your code into **reusable** building blocks.

> With reusable React components [and hooks] it’s trivial to build something awesome. It’s like snapping Lego pieces together. 👍
> 
> — 
> 
> [Cory House](https://medium.com/u/e986f7cdb458?source=post_page-----ca2e47d1bf97--------------------------------)
> 
> , [Designing Reusable React Components](https://medium.com/@housecor/designing-reusable-react-components-1cbeb897b048)

***
##### **Remember this mantra:**

> The art of being a fast developer is an art of writing **reusable** building blocks.

***
# Split apart business logic and view logic

> Life is simpler when UI components are unaware of the network, business logic, or app state. Given the same props, always render the same data.
> 
> — 
> 
> [Eric Elliott](https://medium.com/u/c359511de780?source=post_page-----ca2e47d1bf97--------------------------------)
> 
> , [The Missing Introduction to React](https://medium.com/javascript-scene/the-missing-introduction-to-react-62837cb2fd76)

***

The art of being a fast React developer is an art of separating business logic from view logic.
***
# Split your code into many small reusable files
***
![[frameworks.png]]
***

![[react component.png]]

***
![[react-component-lifestyle.jpg]]
***

#components 
#REACT #react 