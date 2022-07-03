# top level rule
### Only Call Hooks at the Top Level

Don't call hooks inside loops, conditions, or nested functions. Always use hooks at the top level of your React function (component), before any early returns.

The reason behind this is that hooks must be called in the same order each time a component renders. This is what allows React to correctly preserve the state of hooks between multiple useState and useEffect calls.

#hooks #react 
