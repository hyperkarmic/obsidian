# Prop Drilling
## What is Prop drilling?

We create many components and states in React app. These states can be used in other related component. States are passed from parent components to child and grandchild components via Props. This process is called Prop drilling. Let’s continue the topic with the picture below.

![[propdrill.png]]
If we want to pass state in the picture then we have to pass 5 component. In this process, we have to pass state to component that aren’t related to this state. Therefore code redundancy occurs.
***

In this case, we need to pass state from the top level of the application through all the intermediary components to the one which needs the data at the bottom, even though the intermediary levels don't need it. This tedious and time-consuming process is known as _prop drilling_.
***

***

#prop-drilling
#prop-drill #props #react 