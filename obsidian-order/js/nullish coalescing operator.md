


![[nullish.jpg]]

***
```javascript
const zero = 0  
const emptyString = ""  
const defaultValue = "I am the default value."  
  
const orResult1 = zero || defaultValue // "I am the default value."  
const orResult2 = emptyString || defaultValue // "I am the default value."  
  
const nullishResult1 = zero ?? defaultValue // 0  
const nullishResult2 = emptyString ?? defaultValue // ""
```

As you can see, the nullish coalescing operator preserves falsy values that are not null or undefined, whereas the logical OR operator does not.
***
The `??` nullish coalescing operator in JavaScript allows for more concise and accurate handling of `null` and `undefined` values.

By providing a straightforward syntax for dealing with these special cases, JavaScript continues to incorporate functional programming concepts, making it easier for developers to write clean and expressive code.
***



#nullish
#javascript 