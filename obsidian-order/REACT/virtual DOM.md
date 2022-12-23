## Virtual DOM

A virtual DOM is a lightweight JavaScript representation of the DOM used in declarative web frameworks such as React, Vue.js, and Elm.
<hr>

#### **DOM** operations might be really powerful, it comes at a huge cost. It's _one of the slowest operations_ in the world of web dev. To reduce the number of **DOM** operations, we use the **Virtual DOM** to modify the **DOM** if it really requires any modification and not every time something changes.
***
**Virtual DOM:** In basic words, virtual DOM is only a duplicate of the first DOM kept in the memory and synchronized with the genuine DOM by libraries like ReactDOM. This cycle is called Reconciliation.

Virtual DOM has the very properties of the Real DOM, however, it does not have the ability to straightforwardly change the substance of the screen.

-   How Virtual DOM really makes things quicker: When anything new is added to the application, a virtual DOM is made and it is addressed as a tree. Every component in the application is a hub in this tree.

Thus, at whatever point there is an adjustment of the condition of any component, another Virtual DOM tree is made. This new Virtual DOM tree is then contrasted and the past Virtual DOM tree and make a note of the changes.

Later, it tracks down the most ideal ways of rolling out these improvements to the genuine DOM. Presently just the refreshed components will get delivered on the page once more.
***
_The virtual DOM (VDOM) is a programming concept where an ideal, or “virtual”, representation of a UI is kept in memory and synced with the “real” DOM by a library such as ReactDOM. This process is called reconciliation._
- reacts own definition
***
![[virtual-dom.png]]
***
React parses the tree using the Breadth-first search (BFS).

Always keep in mind, Virtual DOM does not physically exist, it’s an in-memory representation or a blueprint of Real DOM.
***
![[virtual-dom2.png]]
***
React cannot afford the cost of repainting all of the DOM nodes after every re-render. To overcome this challenge, React implemented the concept of virtual DOM.

Instead of allowing the browser to redraw all the page elements after every re-render or DOM update, React uses the concept of virtual DOM to figure out what exactly has changed without involving the actual DOM and then ensures that the actual DOM only repaints the necessary data.

This concept helps React optimize performance.
***
## Virtual DOM in React

Virtual DOM in React is a “virtual” representation of the actual DOM. It is nothing but an object created to replicate the actual DOM.

Unlike the actual DOM, the virtual DOM is cheap to create because it doesn’t write to the screen. It is only available as a strategy to prevent a redraw of unnecessary page elements during re-render.
***
However, don’t forget that the virtual DOM is just a simple object representing the UI. Nothing gets drawn on the screen, and so, it is easy to create.

After React creates the new virtual DOM tree, it compares it to the previous snapshot [using a diffing algorithm](https://reactjs.org/docs/reconciliation.html#the-diffing-algorithm) to figure out what changes are necessary.

It then uses [a library called ReactDOM](https://blog.logrocket.com/managing-dom-components-reactdom/) to ensure the actual DOM only receives and repaints the updated node or nodes. This [process is called reconciliation](https://reactjs.org/docs/reconciliation.html).
***
On every render, React has a virtual DOM tree it compares with the previous version to determine what node content gets updated and ensure the updated node matches up with the actual DOM.
***
Whenever we manipulate the virtual DOM elements in React, we bypass the series of operations involved when we directly manipulate the actual DOM.

This is possible because with virtual DOM, nothing gets drawn on the screen. Additionally, with the diffing algorithm, React can finalize what update is necessary and update only the object on the real DOM.
***
Here is a simple analogy to further solidify our knowledge of virtual DOM: Think of manipulating the virtual DOM as editing a structural design or blueprint instead of rebuilding the actual structure.

Editing a blueprint to include an update is very cheap compared to rebuilding the structure every time an update occurs. When the blueprint is revised and finalized, we can then include only the update on the actual structure.
***

#DOM #virtual-dom
#react 