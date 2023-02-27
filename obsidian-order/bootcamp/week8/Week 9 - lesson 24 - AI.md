This exercise demonstrates how to use ES6 template literals to display data. The exercise involves creating a music object and then displaying its properties using template literals in a web page. The code is broken down into three parts:

1.  **music object creation**: The `index.js` file starts by creating a `music` object with three properties: `title`, `artist`, and `album`.
    
2.  **template literal**: The code then defines a `songSnippet` variable that contains a template literal. The template literal includes the `music` object properties as placeholders inside `${}` syntax, which is evaluated and replaced with the corresponding property value. In this case, the `title`, `artist`, and `album` properties of `music` are used to populate the `h2`, `p.artist`, and `p.album` elements, respectively.
    
3.  **rendering to the web page**: Finally, the `element` variable is used to get a reference to the `div` element with the `id` of `music`, and the `songSnippet` variable is inserted into the `innerHTML` of the `element`. The result is that the rendered web page will display the `music` object data inside the `div`.
    

Key code snippets with regard to understanding the exercise:

1.  Creating a music object:

```javascript
const music = {
  title: "The Less I Know The Better",
  artist: "Tame Impala",
  album: "Currents"
};

```

2.  Creating a template literal:

```javascript
const songSnippet = `
  <div class="song">
     <h2>${music.title}</h2>
     <p class="artist">${music.artist}</p>
     <p class="album">${music.album}</p>
  </div>
`;

```

3.  Rendering the template literal to a web page:

```javascript
const element = document.getElementById("music");
element.innerHTML = songSnippet;



