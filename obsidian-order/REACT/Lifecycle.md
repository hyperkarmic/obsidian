[Lifecycle](https://pandaquests.medium.com/lifecycle-methods-in-reactjs-78dcda71cc61) methods: Lifecycle methods are functions that are called at different stages of a component's lifecycle, such as when it is mounted, updated, or unmounted. Understanding these methods can help you better control the behavior of your components.
***
Lifecycle methods in ReactJS are functions that are called at specific points during the lifecycle of a component, which is a piece of code that represents a part of a user interface (UI) in a web application. These methods allow you to control how a component is created, rendered, and updated in the UI.
***

There are several different lifecycle methods in ReactJS, but some of the most common ones are:

-   componentDidMount(): This method is called when a component is first added to the UI. It’s often used to trigger actions that should happen after the component is rendered, such as fetching data from an API or setting up event listeners.
-   shouldComponentUpdate(): This method is called before a component is updated in the UI. It allows you to control whether or not the component should be re-rendered based on certain conditions. For example, you might use this method to prevent a component from being re-rendered if its props (input data) haven’t changed.
-   componentDidUpdate(): This method is called after a component has been updated in the UI. It’s often used to trigger actions that should happen after the component is updated, such as updating the value of a form field or displaying a notification message.
-   componentWillUnmount(): This method is called just before a component is removed from the UI. It’s often used to clean up any resources that were created by the component, such as event listeners or timers.
#react #lifecycle 