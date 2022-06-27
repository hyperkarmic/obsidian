# REACT CONTEXT
# What is Context?

A Context is basically a JavaScript object that can be passed from one parent component to several child components efficiently. Props can pass values to components as well. But, if a value needs to be passed to a child component deep in the component tree, using props means the value also passes through components that do not need it. Or, if a value is required by several components, props can make it difficult.
***
## **Context API**
Context provide to access data from whole components without having to pass props down manually at every level. We can create global variables in the Context API and arrive to them form any component. So we don’t need to pass props to other components and we write clean code. This situation add flexibility to application and improves code readability and clarity. Besides, operating cost and intensity are reduced
***
![[context.png]]
***
##### good things

1.  Context provides to directly accessibility from components.
2.  Reduces time and labor cost.
3.  Adds dynamism and flexibility to the application.
4.  Improves the readability of the code.
5.  Easy to use and learn.
6.  No need to install any packages for using, this reduces dependency.

# bad things
1.  Context API isn’t suitable for data that is frequently refreshed or changed.
2.  As the application grows, it can become more difficult to use.
3.  Reuse components can be harder as some data come from context, not always from Props.
***

-   React Context is a method to pass props from parent to child component(s), by storing the props in a store and using these props from the store by child component(s) without actually passing them manually at each level of the component tree.
-   In a typical React application, data is passed top-down (parent to child) via props, but such usage can be cumbersome for certain types of props (e.g. locale preference, UI theme) that are required by many components within an application. Context provides a way to share values like these between components without having to explicitly pass a prop through every level of the tree.
***
# Where we use Context in React ?

-   Whenever one wants a store to keep states or variables in and use them elsewhere in program, Context is used. Generally, when we have two or more levels(height) in our component tree, it is viable to use a store instead of passing props and then lifting the state as this will create confusion and unnecessary lengthy code.
-   Context is designed to share data that can be considered “global” for a tree of React components, such as the current authenticated user, theme, or preferred language.

# What are the Benefits of the context in React ?

-   One of the most important things about React is that the data flows in only one direction, which enables the developers to predict.
-   It enables easy debugging.
-   It provides Reusability.

Context lets us pass a value deep into the component tree without explicitly threading it through every component.
***
## With the context API, we can avoid passing props through intermediate elements, and directly pass the props to the last child or the child we are targeting:
***
## Every Context object comes with a Provider React component that allows consuming components to subscribe to context changes. All that we have to do is make a variable (here it is initialState) and give it and the provider an initial value. This initial value depends upon the project which you are making.
***
Hence , React Context API is a way to essentially create global variables that can be passed around in a React app. This is the alternative to “prop drilling”, or passing props from grandparent to parent to child, and so on.
***
This is where Context API comes in. It provides a way of passing data through the component tree via a Provider-Consumer pair without having to pass props down through every level. Think of it as the components playing Catch with data - the intermediary components might not even "know" that anything is happening:
***
Like all good things in code, there are some caveats to using Context:

-   **Don't use Context to avoid drilling props down just one or two layers.** Context is great for managing state which is needed by large portions of an application. However, prop drilling is faster if you are just passing info down a couple of layers.
    
-   **Avoid using Context to save state that should be kept locally.** So if you need to save a user's form inputs, for example, use local state and not Context.
    
-   **Always wrap the Provider around the lowest possible common parent in the tree - not the app's highest-level component.** No need for overkill.
    
-   **Lastly, if you pass an object as your value prop, monitor performance and refactor as necessary.** This probably won't be needed unless a drop in performance is noticeable.
***
[React's Context API](https://reactjs.org/docs/context.html) is a popular choice for global state _(my definition: state that is shared amongst components)_. It is easy to use and we are used to it because a lot of libraries leverage them. There are characteristics of React Context that you should be aware of. They make context not always the best choice for global state.

## Why Does React Context Exist?

Technically we could just place our whole state at our top-level component and pass it down the React element tree to the components that need access to the state. But in any application but a very simple one that would require us to pass down the state several levels down the tree and through components that are not using the state themselves at all. It would pollute the code and ruin the Developer Experience (DX). That problem is known as **prop-drilling**. React's Context API was created to mitigate this issue. This is an excerpt from the [React Context API docs](https://reactjs.org/docs/context.html):

> Context provides a way to pass data through the component tree without having to pass props down manually at every level.

By combining React's state-related hooks (`useState` and `useReducer`) with React context you can provide a shared state to all components nested within the contexts `Provider`. Problem solved, right? Well, no. 

#react #context
