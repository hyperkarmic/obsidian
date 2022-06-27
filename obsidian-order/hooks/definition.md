# React Hooks Definitions:
### Hooks allow function components to have access to state and other React features. Because of this, class components are generally no longer needed.
<hr>

## Hooks allow us to "hook" into React features such as state and lifecycle methods.
<hr>
## u must `import` Hooks from `react`.
<hr>

## React Hooks are in-built functions that allow React developers to use state and lifecycle methods inside functional components, they also work together with existing code, so they can easily be adopted into a codebase.
<hr>

## Hooks are simply functions that allow you to **hook into** or **make use of** React features.
<hr>
## This essentially means that Hooks are functions that 'hook' into [React state](https://javarevisited.blogspot.com/2021/09/how-to-use-state-in-react-example.html) and [lifecycle features](https://www.java67.com/2021/09/ow-to-use-lifecycle-methods-in-functinal.html) from inside the function components.
<hr>
**Hooks apply the React philosophy (explicit data flow and composition) _inside_ a component, rather than just _between_ the components.**
<hr>
Hooks solve exactly that problem. Hooks let you use React features (like state) from a function — by doing a single function call. React provides a few built-in Hooks exposing the “building blocks” of React: state, lifecycle, and context.
<hr>
I believe that Hooks are a bridge to Redux but also a way of managing simple state without introducing Redux.
<hr>

With the introduction of [React Hooks](https://reactjs.org/docs/hooks-intro.html), you’ll get to use a state and manage the class-based lifecycle logic inside of the function components.
<hr>
[React Hooks](https://reactjs.org/docs/hooks-intro.html) (introduced in React since version 16.8) are JavaScript functions that allow us to build our React component ONLY with a function component.
<hr>
Previously, React features such as state and lifecycle functions are available only for class-based components. Function-based components are referred to as dumb, skinny, or just presentational components because they can’t have access to state and lifecycle functions.

But since the release of React Hooks, function-based components have been elevated into first-class citizens of React. It has enabled function components to compose, reuse, and share React code in new ways.
<hr>
They allow you to use state and other React features without writing a class. They are a powerful way to write stateful components, and they are a great way to write functional components.
<hr>
1.  The first reason is that working with classes can sometimes bring on certain problems and extra things to worry about. For example, understanding how the **this** keyword works in JavaScript and remembering to bind event handlers in class components. Classes also don’t minify very well and make hot reloading unreliable.
2.  The second reason touches on some of the more advanced React topics, such as higher-order components and the render props pattern. If you’ve worked with React, you’ll know that there is no particular way to reuse stateful component logic between components. The HOC (higher-order component) and render props patterns do address this problem, however you have to restructure your components (such as wrapping your components with several other components) which can result in awkward or poor looking code that is harder to follow. There is a need to share stateful logic in a better way, and this is where Hooks can help, as they allow us to reuse stateful logic without changing the component hierarchy.
3.  The third reason has to do with how code is placed in a component, and the fact that complex components can become hard to understand. When creating components for complex scenarios such as data fetching and subscribing to events, you’ll realize that the related code is not organized in one place but rather scattered across different lifecycle methods. For example, data fetching is usually done in componentDidMount and also sometimes in componentDidUpdate. Another example is setting event listeners in componentDidMount and componentWillUnmount. As you can see, related code is separated in different methods but at the same time completely unrelated code such as data fetching and event listeners end up in the same code block (componentDidMount). In an ideal world all related code would be together, but because of stateful logic, components cannot be broken down into smaller ones. Thankfully, Hooks solve this problem as well because rather than forcing a split based on lifecycle methods, Hooks let you split one component into smaller functions based on what pieces are related.
<hr>
###### The main reasons for the introduction of Hooks are: **a.** By not having to use classes, Hooks avoid the confusion of the **this** keyword and components minify better **b.** Hooks allow you to reuse stateful logic without changing your component hierarchy, and you can avoid advanced React patterns making your code much simpler to follow, and **c.** Hooks let us organize the logic inside a component into reusable isolated units, and related code can be put together helping to avoid bugs and inconsistencies
<hr>
What is react hooks ? Hooks allow function components to have access to state and other React features. Because of this, class components are generally no longer needed. Hooks allow us to “hook” into React features such as state and lifecycle methods
***
Hooks:So what about hooks? **Well they return variables and functions** rather than JSX.
***

A Hook has two phases: mount and update.

The mount function is executed when the hook is created for the first time, and the update function is executed every time the hook is updated there after!

![[life-cyce.png]]

***

#react #hooks
#definition 
