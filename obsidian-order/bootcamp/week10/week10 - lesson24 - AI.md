The Word Guess game is a command-line game where the user guesses a word by inputting letters. The game is designed using Object-Oriented Programming principles and consists of three files, `Letter.js`, `Word.js`, and `index.js`. The `Letter.js` file contains the `Letter` class, which is used to create letter objects. The `Word.js` file contains the `Word` class, which uses the `Letter` class to create word objects. Finally, the `index.js` file contains the game's logic, which randomly selects a word and prompts the user for each guess.

The `Letter.js` file contains a class that has the following properties:

-   A string value to store the underlying character for the letter
-   A boolean value that stores whether that letter has been guessed yet

The class also has two methods:

-   A function that returns the underlying character if the letter has been guessed, or a placeholder (like an underscore) if the letter has not been guessed
-   A function that takes a character as an argument and checks it against the underlying character, updating the stored boolean value to true if it was guessed correctly

The `Word.js` file contains a class that has the following properties:

-   An array of `new` `Letter` objects representing the letters of the underlying word

The class also has two methods:

-   A function that returns a string representing the word. This should call the function on each letter object (the first function defined in `Letter.js`) that displays the character or an underscore and concatenate those together.
-   A function that takes a character as an argument and calls the guess function on each letter object (the second function defined in `Letter.js`)

The `index.js` file contains the game's logic, which does the following:

-   Randomly selects a word and uses the `Word` class to store it
-   Prompts the user for each guess and keeps track of the user's remaining guesses

The `Letter.js` file does not require any other files, and the `Word.js` file only requires `Letter.js`.

The `Letter.test.js` and `Word.test.js` files contain test cases for the `Letter.js` and `Word.js` files, respectively. The tests ensure that the classes are working as expected.

Here are the key code snippets for better understanding:

`Letter.js` class:

```javascript
class Letter {
  constructor(character) {
    this.character = character;
    this.guessed = false;
  }

  toString() {
    if (this.guessed) {
      return this.character;
    } else {
      return "_";
    }
  }

  guess(letter) {
    if (letter === this.character) {
      this.guessed = true;
      return true;
    } else {
      return false;
    }
  }
}

```

`Word.js` class:

```javascript
class Word {
  constructor(word) {
    this.letters = [];
    for (let i = 0; i < word.length; i++) {
      this.letters.push(new Letter(word[i]));
    }
  }

  toString() {
    let wordString = "";
    for (let i = 0; i < this.letters.length; i++) {
      wordString += this.letters[i].toString();
    }
    return wordString;
  }

  guessLetter(letter) {
    let foundLetter = false;
    for (let i = 0; i < this.letters.length; i++) {
      if (this.letters[i].guess(letter)) {
        foundLetter = true;
      }
    }
    return foundLetter;
  }
}

```

index.js

```javascript
const Word = require("./Word");
const inquirer

```
