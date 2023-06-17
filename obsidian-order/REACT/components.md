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
[Components](https://pandaquests.medium.com/components-in-reactjs-3974f7a65874): In React, a component is a piece of code that represents a part of the UI. Components can be reused throughout the app, which helps make the code more reusable and easier to maintain.
***
A component in ReactJS is a piece of code that simulates a certain user interface element (UI). You can use it as a little building piece to create more intricate UI elements.
***
Components in ReactJS offer several advantages:

-   Reusability: You may create reusable user interface (UI) components using components, allowing you to reuse the same component across different areas of your app. You won’t have to write the same code repeatedly, which can save a lot of time and work.
-   Maintainability: The self-contained nature of the components makes it simpler to maintain and upgrade your project. If a component needs to be changed, you just need to make the change once, and it will be reflected everywhere the component is used.
-   Readability: If you give your components names that are descriptive, components might make your code simpler to read and comprehend. This can be extremely useful, if you’re working in a group or need to return to your code after a break.
-   Testability: Components are easy to test one by one, which can save you time and effort when writing and debugging your code.
-   Scalability: Because you can simply reuse existing components and create new ones as needed, components make it easier to scale your app as it expands.
***
Components in ReactJS can be used in a variety of ways:

-   Building UI elements: Components can be used to build UI elements such as buttons, forms, lists, and more. This can save you time and effort, as you can reuse these components throughout your app.
-   Organizing code: Components can help you organize your code into logical pieces, which can make it easier to understand and maintain.
-   Sharing state: Components can share state (data) with each other through props (short for properties) and state. This can be especially helpful if you have data that needs to be displayed or used in multiple places throughout your app.
-   Abstracting complexity: Components can help you abstract complexity by breaking your app down into smaller, more manageable pieces. This can make it easier to understand and work with your code.
-   Testing: Components can be tested in isolation, which can save you time and effort when debugging and ensuring the quality of your code.
***
## **𝗧𝗵𝗲 𝟰 𝗯𝗶𝗴𝗴𝗲𝘀𝘁 𝗺𝗶𝘀𝘁𝗮𝗸𝗲𝘀 𝗼𝗳𝘁𝗲𝗻 𝗺𝗮𝗱𝗲 𝘄𝗵𝗲𝗻 𝗯𝘂𝗶𝗹𝗱𝗶𝗻𝗴 𝗰𝗼𝗺𝗽𝗼𝗻𝗲𝗻𝘁𝘀**

Here are some of the biggest mistakes leading to nothing but pain and frustration when maintaining components:

-   Building complex components
-   Adding multiple responsibilities to single components
-   Building components coupled with several moving parts
-   Adding business logic in components
***
![[compo.jpg]]
***
![[compos.jpg]]


#components 
#REACT #react 