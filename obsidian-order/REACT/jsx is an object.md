# jsx is an object!!!!!
![[jsx-object.jpeg]]


It’s true that Component returns JSX, but JSX is a special syntax which JavaScript can’t read directly. Instead, it requires transpilers to turn it into **createElement** calls, which are just JavaScript plain objects. Depending on your stack, the transpilation can be done either by **Babel** or **TypeScript**. That’s why you always have to `import React from ‘react’` to write JSX, because it needs to run `React.createElement` , so `React` needs to be in scope. Since React 17, there is a new JSX Transform — there’s no requirement for that import anymore, in case you’re curious, read more [here](https://reactjs.org/blog/2020/09/22/introducing-the-new-jsx-transform.html).

#JSX 
#object 