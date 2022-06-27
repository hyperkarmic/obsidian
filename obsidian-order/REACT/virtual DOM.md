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


#DOM #virtual-dom
#react 