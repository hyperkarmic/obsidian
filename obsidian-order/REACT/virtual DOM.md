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
[The Virtual DOM](https://pandaquests.medium.com/the-virtual-dom-in-reactjs-85ed233eaa99): The Virtual DOM is a lightweight in-memory representation of the actual DOM. React uses the Virtual DOM to determine the minimum number of changes that need to be made to the actual DOM when the state of a component changes. This helps improve the performance of React apps by minimizing the number of DOM updates.
***
The Virtual DOM is a crucial concept in ReactJS, a JavaScript library for building user interfaces. Knowing how to handle the virtual DOM will make you a better ReactJS developer. It is an abstract representation of the actual DOM (Document Object Model) and enables efficient updates to the actual DOM by minimizing the number of DOM manipulations required. The Virtual DOM plays a vital role in the performance and efficiency of React applications.
***
Imagine that you have a website with a large amount of content, and you want to make a small change to one piece of that content. If you were to update the content directly on the website, the entire page would have to be re-rendered, which can be time-consuming and slow.

The Virtual DOM helps solve this problem by creating a virtual representation of the website’s actual DOM (Document Object Model). The DOM is a tree-like structure that represents the structure of a website, including all of its elements and their relationships to one another.

When you make a change to the website, the Virtual DOM creates a new virtual representation of the updated DOM and compares it to the previous version. It then identifies the specific changes that need to be made and only updates those elements on the actual DOM, rather than re-rendering the entire page.
***
Some common use cases for the Virtual DOM include:

-   Updating dynamic content: If your web application displays content that frequently changes, such as a news feed or a chat room, the Virtual DOM can help improve the performance of these updates by only updating the specific elements that have changed.
-   Handling user input: The Virtual DOM can also be useful when handling user input, such as form submissions or button clicks. It can help ensure that the DOM updates smoothly and efficiently in response to user actions.
-   Displaying large lists of data: If your web application displays a large amount of data, such as a list of products or a table of data, the Virtual DOM can help improve the performance of these updates by minimizing the number of DOM updates and re-renders that need to take place.
-   Creating smooth animations: The Virtual DOM can also be used to create smooth and efficient animations in your React applications. By minimizing the number of DOM updates, the Virtual DOM can help ensure that your animations run smoothly and without interruption.
***
### Limitations of the Traditional DOM approach

-   Performance: The conventional DOM technique can be time-consuming and memory-intensive for large documents. The reason for this is because the entire page is loaded into memory, it must be updated every time something is changed, which can take some time.
    
-   Complexity: Working with the DOM tree can be challenging, especially for developers new to web programming. As a result, the code could be challenging to read, comprehend, and maintain.
    
-   Restricted interactivity: The conventional DOM technique is not optimal for dynamic, interactive applications. While filling out a form, the user may need to render the entire document each time they enter a new character, which can be tedious and cumbersome.
    
-   Difficulty of scalability: Scaling large, sophisticated applications using the conventional DOM method is difficult. The DOM tree can become cumbersome and challenging to manage as the application expands in size and complexity.
    

### Benefits of working with the Virtual DOM

-   Improved user experience: The virtual DOM can offer a better user experience by requiring less work to update the DOM. Applications created with the help of the virtual DOM can refresh their user interface more quickly, react to user interactions more quickly, and offer a more seamless experience in general.
    
-   Development Process Optimized: The virtual DOM optimizes development by using a declarative programming model. Developers may now declare how they want the application to look, and the virtual DOM will take care of the rest, according to this. This strategy can lessen the amount of code required, increase readability, and facilitate codebase maintenance.
    
-   Increased performance: By lowering the number of updates required to the actual DOM, the virtual DOM can greatly increase the performance of online applications. Instead of modifying the actual DOM directly, it accomplishes this by constructing a virtual version of the DOM and making changes to it. Once all the updates have been completed, the virtual DOM only makes the necessary updates to the actual DOM, minimizing the overall amount of work required.
***
![[react-dom.jpg]]
***
![[reactive-updates.jpg]]
***

![[virt-dom.jpg]]

***
![[virtual-dom.jpg]]

#DOM #virtual-dom
#react 