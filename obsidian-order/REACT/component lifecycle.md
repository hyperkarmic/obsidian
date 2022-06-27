# Component Lifecycle
Every single part utilized in React has its lifecycle which can be checked and controlled in the three periods of its Lifecycle. In React, the life cycle of a component represents the different stages of the component during its existence. React provides a callback function to attach functionality in each and every stage of the React life cycle.

The three fundamental periods of a React Component’s lifecycle are:

-   Mounting
-   Updating
-   Unmounting

1.  **Mounting:** Mounting refers to the method involved with placing the various components in the DOM. There are four unique built-in methods or techniques when mounting a component. And that is brought in a specific request composed beneath to mount apart:

-   **Constructor():** The constructor() method is called before anything else when the component is initiated, and it is the natural place to set up the initial state and other initial values.

The constructor() method is called with the props, as arguments, and you should always start by calling the super(props) before anything else, this will initiate the parent’s constructor method and allow the component to inherit methods from its parent (React. Component).

The constructor method is called by React every time when we make a component:

**2. Updating:** Updating the part is considered the second stage in the part lifecycle. At whatever point there is an adjustment of the condition of the part, the part should be refreshed. A component is updated whenever there is a change in the component’s state or props. For refreshing, there are five techniques utilized and are brought in the request beneath. In this order, a component is updated:

**3. Unmounting:**

The next phase or last stage in the Component lifecycle is the Unmounting stage. When a component is removed from the DOM or unmounting as React likes to call it. React has only one built-in method that gets called when a component is unmounted: componentWillUnmount().

#react #REACT #coponent-lifecycle
