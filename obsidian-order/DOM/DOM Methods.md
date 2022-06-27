# DOM Javascript Methods

`getElementById()`
This code tells the computer to get the `<p>` element with the `id` of `para1` and print the element to the console.

```js
const paragraph1 = document.getElementById("para1");
console.log(paragraph1);
```
***

`querySelector()`
##### You can use this method to find elements with one or more CSS selectors.
```js
const h1Element = document.querySelector("h1");
console.log(h1Element);
```
***

`querySelectorAll()`
##### This method finds all of the elements that match the CSS selector and returns a list of all of those nodes.

If I wanted to find all of the `<li>` items in our example, I could use the `>` child combinator to find all of the children of the `<ul>`.

```js
const listItems = document.querySelectorAll("ul > li");
console.log(listItems); 
```
***
Accessing the DOM is essential for getting the most out of your program, but doing so repeatedly causes visual clutter and will slow down the program.

Instead, access it once and cache it for later use in a variable. From then on, you can access that variable instead of the DOM directly. This process is visually cleaner and more efficient.
***

#DOM #Methods
#javascript #js 