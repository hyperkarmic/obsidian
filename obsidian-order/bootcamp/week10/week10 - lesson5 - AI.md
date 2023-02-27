This code demonstrates the use of prototypes in JavaScript.

1.  The first section demonstrates some basic array methods, including forEach and map, which are prototype methods. It also demonstrates how to log out a variable to the console using console.log, which is also a built-in prototype method.
    
2.  The second section demonstrates how to create and work with an object in JavaScript. It shows how to access properties of an object, and how to use built-in prototype methods like toLowerCase and toString.
    
3.  The third section demonstrates how to use prototypes to create a constructor function for creating objects. It creates a Movie constructor function that takes in a title and releaseYear as arguments, and then defines a logInfo method on the Movie prototype. It then creates a new instance of the Movie constructor and calls the logInfo method on that instance.
    

Here are some key code snippets with explanations:

-   Creating a constructor function and defining a prototype method:

```javascript
function Movie(title, releaseYear) {
  this.title = title;
  this.releaseYear = releaseYear;
}

Movie.prototype.logInfo = function () {
  console.log(`${this.title} was released in ${this.releaseYear}`);
};

```

In this code, we define a Movie constructor function that takes in a title and releaseYear as arguments. We then define a logInfo method on the Movie prototype using the prototype keyword. This allows us to create new instances of the Movie object that have access to the logInfo method.

-   Creating a new instance of an object and calling a prototype method:

```javascript
const theShining = new Movie("The Shining", 1980);
theShining.logInfo();

```

In this code, we create a new instance of the Movie object called theShining, passing in "The Shining" as the title and 1980 as the releaseYear. We then call the logInfo method on theShining, which logs out the movie information to the console.

-   Checking if an object has a property or method defined on it vs its prototype:

```javascript
console.log(theShining.hasOwnProperty("title"));
console.log(theShining.hasOwnProperty("logInfo"));
console.log(Movie.prototype.hasOwnProperty("logInfo"));

```

In this code, we use the hasOwnProperty method to check if theShining object has a "title" property and a "logInfo" method defined on it. We also check if the logInfo method is defined on the Movie prototype using Movie.prototype.hasOwnProperty("logInfo"). This shows how we can use prototypes to add methods to objects, without cluttering the object's own properties.