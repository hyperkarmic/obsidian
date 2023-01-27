# Props
### Props:Pass data from a parent component, to a child component, in React…..
<hr>

![[Pasted image 20220425020924.png]] 

***
# React Props Overview

Props are really a short form notation for properties and they are mainly used to transfer data between React components. A common use of props is to pass data from a parent component to a child component using props.

An important point to mention is that React encourages allowing the passing of data from parent to child components only and not the other way around. Although there are ways to pass data from child to parent components([Here is a link](https://stackoverflow.com/questions/38394015/how-to-pass-data-from-child-component-to-its-parent-in-reactjs) to a Stack Overflow post showing how to do this), this is not looked at as a best practice and should generally be avoided when possible. This practice is looked down upon because of the React’s philosophical principle of unidirectional data flow.
***
# What are props in React?

Props are the short form of properties that we can pass between the parent and the child component and can use it as we want but cannot change its values as they are read-only **properties.**

As told above, they can easily make the flow of the app dynamic

We can pass everything as props to the child component, especially functions that will help in updating the state of the parent component.
***

Let’s first discuss how we can use props in our child component. There are mainly three ways of doing it –

1.  With destructuring
2.  Without destructuring
3.  Using defaultProps
***
Props is any data passed into a React Component [props=”value”]. It helps to make components dynamic.
***
## What Are Props in React?

Props simply stands for properties. They are what make components reusable. Because they perform an essential function – they pass data from one component to another.  

Props act as a channel for component communication. Props are passed from parent to child and help your child access properties that made it into the parent's tree.
***
-   We use props in both functional and class-based components.
-   We pass props from the top to bottom. We can also refer to it as ancestor to descendant, or parent to child.
-   Props are read-only. This means that once a component receives a bunch of props, we cannot change it, but we can only use and consume it and cannot modify the properties passed down to the component. If we want to modify that, we'll have to introduce what we call state in React.
***


	
	
	Adding props to a component is pretty simple
BlogPostComponent  
title='First post'  
subtitle='Created by me'
/>
***
![[props v comp.png]]
***
![[props.jpg]]
***
[Props](https://pandaquests.medium.com/props-in-reactjs-3f24d6414d2c): Props are a way to pass data from a parent component to a child component. They are read-only in the child component and are used to customize the child component's behavior.
***
Props are short for “properties” in ReactJS. They are pieces of information received by a component from its parent component.
***
To conclude, while props are a valuable tool in ReactJS, it’s important to use them appropriately and not rely on them too heavily. In some cases, other features like state or context may be better suited to manage data in your application.

Props in ReactJS are used to pass data from a parent component to a child component.
***
