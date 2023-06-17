
## The falsy values in JavaScript are `0`, `0n`, `null`, `undefined`, `false`, `NaN`, and the empty string `""`. They evaluate to false when coerced by JavaScript’s typing engine into a boolean value, but they are not necessarily equal to each other.
***
“A **falsy** value is a value that is considered false when encountered in a [Boolean](https://developer.mozilla.org/en-US/docs/Glossary/Boolean) context.” — [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Glossary/Falsy)
***
In JavaScript, there is a special list of following 7 values, which are called [falsy values](https://developer.mozilla.org/en-US/docs/Glossary/Falsy) — they all evaluate to false in conditionals:

-   the [number](https://medium.com/coding-in-simple-english/how-to-check-for-nan-in-javascript-4294e555b447) `0`. (and [-0](https://medium.com/coding-at-dawn/is-negative-zero-0-a-number-in-javascript-c62739f80114))
-   the [BigInt](https://levelup.gitconnected.com/how-to-check-if-a-number-is-a-bigint-in-javascript-6d658be6e89c) `0n`
-   the keyword `[null](https://javascript.plainenglish.io/how-to-check-for-null-in-javascript-dffab64d8ed5)`
-   the keyword `[undefined](https://medium.com/coding-at-dawn/how-to-check-for-undefined-in-javascript-bcedd62c8ad)`
-   the [boolean](https://javascript.plainenglish.io/how-to-check-for-a-boolean-in-javascript-98fdc8aec2a7) `false`
-   the number `[NaN](https://medium.com/coding-in-simple-english/how-to-check-for-nan-in-javascript-4294e555b447)`
-   the empty string `[""](https://javascript.plainenglish.io/the-real-difference-between-single-quotes-and-double-quotes-in-javascript-3d00bf720bcd)` (equivalent to `[''](https://javascript.plainenglish.io/the-real-difference-between-single-quotes-and-double-quotes-in-javascript-3d00bf720bcd)` or `[``](https://javascript.plainenglish.io/are-backticks-slower-than-other-strings-in-javascript-ce4abf9b9fa)`)

Strictly speaking, you have to “coerce” (force) a falsy value to make it `false`, for example by using `[Boolean()](https://javascript.plainenglish.io/how-to-check-for-a-boolean-in-javascript-98fdc8aec2a7)` or [the](https://javascript.plainenglish.io/how-to-check-for-a-boolean-in-javascript-98fdc8aec2a7) `[?](https://javascript.plainenglish.io/how-to-check-for-a-boolean-in-javascript-98fdc8aec2a7)` [ternary operator](https://javascript.plainenglish.io/how-to-check-for-a-boolean-in-javascript-98fdc8aec2a7).
***
Truthy values include the empty object `{}` and the empty array `[]` — since they aren’t falsy, they are truthy, by definition.
***
Despite all being falsy, they are not all equal with the double equals `==`:

1.  The values `null` and `undefined` are loosely equal to each other.
2.  `NaN` is not equal to any other value, not even itself.
3.  The other falsy values (`0`, `0n`, `false`, and `""`) are all loosely equal.
***



#js #javascript #falsy 