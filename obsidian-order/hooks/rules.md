## Hooks rules
## Hook Rules

There are 3 rules for hooks:

-   Hooks can only be called inside React function components.
-   Hooks can only be called at the top level of a component.
-   Hooks cannot be conditional

**Note:** Hooks will not work in React class components.
<hr>
**Rules to use Hooks:**

1.  Only call Hooks from React functions,
2.  Only Call Hooks at the Top Level.
3.  Hooks can call other Hooks

Don't call Hooks inside loops, conditions, or nested functions. Instead, always use Hooks at the top level of your React function. By following this rule, you ensure that Hooks are called in the same order each time a component renders. That's what allows React to correctly preserve the state of Hooks between multiple useState and useEffect calls.

Don’t call Hooks from regular JavaScript functions. Instead, you can:

-   Call Hooks from React function components.
-   Call Hooks from custom Hooks.
<hr>


#hooks #react #rule