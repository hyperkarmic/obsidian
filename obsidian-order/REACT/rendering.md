# rendering
Rendering is a process when React finds out how the layout tree should be, it happens when mounting and updating. During the update, Reconciliation is executed to collect the difference between the new tree and the old tree, once a component is marked needing update, React re-renders all of its children, even those child components stay unchanged. In this regard, wasted renders appear and might cost much effort,
***

## [What is re-render in React?](https://www.developerway.com/posts/react-re-renders-guide#part1)

When talking about React performance, there are two major stages that we need to care about:

-   **initial render** - happens when a component first appears on the screen
-   **re-render** - second and any consecutive render of a component that is already on the screen

Re-render happens when React needs to update the app with some new data. Usually, this happens as a result of a user interacting with the app or some external data coming through via an asynchronous request or some subscription model.

Non-interactive apps that don’t have any asynchronous data updates will **never** re-render, and therefore don’t need to care about re-renders performance optimization.
***
**Every re-render in React starts with a state change.** It's the only “trigger” in React for a component to re-render.*

Here's the thing: when a component re-renders, **it also re-renders all of its descendants.**

_Big Misconception #1_: **The entire app re-renders whenever a state variable changes.**

 _Big Misconception #2_: **A component will re-render because its props change.**
 **props have nothing to do with re-renders.**
 

***

#REACT #rendering