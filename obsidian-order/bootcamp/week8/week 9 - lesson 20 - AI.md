This is a simple exercise that involves converting an existing JavaScript application from using ES5 syntax to ES6 syntax. The application is a guessing game where the user is presented with three colored crystals. Each crystal has a random point value, and when clicked, adds its point value to the user's score. The goal of the game is to match the target score, which is also randomly generated.

The readme.md file provides instructions for the developer to:

1.  Open the `index.html` file in their web browser and understand the application's functionality.
2.  Open the `index.js` file in their code editor and convert the code over to use the ES6 syntax.
3.  Convert all `var` identifiers to use `const` or `let` - whichever is more appropriate.
4.  Convert functions to arrow functions where suitable - remembering that arrow functions are not right for every situation.

The learning outcomes for this exercise are to familiarize the developer with using `const` and `let` instead of `var`, and to introduce them to arrow functions.

Here are some key code snippets that illustrate the changes required to convert the code from ES5 to ES6 syntax:

1.  Replacing `var` with `const` or `let`:

```javascript
// ES5
var score;
var targetScore;

// ES6
let score;
let targetScore;

```

2.  Converting function declarations to arrow functions:

```javascript
// ES5
function makeGuess() {
  // function body
}

// ES6
const makeGuess = () => {
  // function body
};

```

3.  Using template literals instead of concatenation:

```javascript
// ES5
$score.textContent = "Score: " + score + " | " + "Target: " + targetScore;

// ES6
$score.textContent = `Score: ${score} | Target: ${targetScore}`;

```

4.  Converting constructor functions to classes:

```javascript
// ES5
const Crystal = function(color) {
  // constructor body
};

Crystal.prototype.render = function(target) {
  // method body
};

// ES6
class Crystal {
  constructor(color) {
    // constructor body
  }

  render(target) {
    // method body
  }
}

```

Replacing `document.createElement` with template literals

```javascript
// ES5
this.element = document.createElement("div");
this.element.className = "crystal " + color;

// ES6
this.element = `<div class="crystal ${color}"></div>`;

```

These changes should help the developer become more familiar with the ES6 syntax, and the use of `const`, `let`, and arrow functions in JavaScript.