## Introduction:

This exercise is about Object-Relational Mapping (ORM) and Sequelize, which is an ORM for Node.js applications. The purpose of this exercise is to create a simple web application that allows users to add, view, and delete information from a database.

## Code overview:

The code is structured into multiple folders and files. Here is a brief overview of each:

1.  `package.json`: This file is used to manage the dependencies and configuration of the project.
    
2.  `server.js`: This is the main file that starts the server and sets up the API and HTML routes.
    
3.  `schema.sql`: This file contains the SQL schema for the database.
    
4.  `config/connection.js`: This file sets up the database connection.
    
5.  `config/orm.js`: This file contains the Object-Relational Mapping (ORM) logic.
    
6.  `routes/api-routes.js`: This file defines the API routes.
    
7.  `routes/html-routes.js`: This file defines the HTML routes.
    
8.  `public/add.html`, `public/all.html`, and `public/view.html`: These files define the HTML templates for adding, viewing, and deleting data.
    
9.  `public/js/add.js`, `public/js/all.js`, and `public/js/view.js`: These files define the JavaScript logic for adding, viewing, and deleting data.
    

## Learning outcomes:

Through this exercise, you will learn how to use Sequelize, which is a powerful ORM for Node.js. You will learn how to:

1.  Set up a database connection using Sequelize.
    
2.  Define Sequelize models and map them to database tables.
    
3.  Perform CRUD (Create, Read, Update, Delete) operations on the database using Sequelize.
    
4.  Define and use API routes to interact with the database.
    
5.  Define and use HTML routes to render HTML templates.
    
6.  Use JavaScript to interact with the API and HTML routes.
    

## Steps:

1.  First, create a new Node.js project and install the necessary dependencies, such as Express and Sequelize.
    
2.  Next, set up the database connection in the `config/connection.js` file.
    
3.  Define the Sequelize models in the `config/orm.js` file.
    
4.  Define the API routes in the `routes/api-routes.js` file.
    
5.  Define the HTML routes in the `routes/html-routes.js` file.
    
6.  Define the JavaScript logic for adding, viewing, and deleting data in the `public/js` folder.
    

## Code snippets:

Here are some key code snippets for understanding the exercise:

1.  Defining a Sequelize model:

```javascript
module.exports = function(sequelize, DataTypes) {
  var Book = sequelize.define("Book", {
    title: DataTypes.STRING,
    author: DataTypes.STRING,
    genre: DataTypes.STRING
  });
  return Book;
};

```

In this code snippet, we define a Sequelize model called "Book". The model has three columns: "title", "author", and "genre".

2.  Setting up a database connection:

```javascript
var sequelize = new Sequelize("database_name", "user", "password", {
  host: "localhost",
  dialect: "mysql"
});

```

In this code snippet, we set up a database connection using Sequelize. We specify the database name, username, password, host, and dialect (in this case, MySQL).

3.  Defining an API route:

```javascript
app.get("/api/books", function(req, res) {
  db.Book.findAll({}).then(function(result) {
    res.json(result);
  });
});

```

In this code snippet, we define an API route that retrieves all books from the database and returns them as JSON.

4.  Defining an HTML route:

```javascript
app.get("/add", function(req, res) {
  res.sendFile(path.join(__dirname, "../public/add.html"));
});

```

In this code snippet, we define an HTML route that renders the `add.html` template when a user visits the `/add` URL.

5.  JavaScript logic for adding data:

```javascript
$("#add-btn").on("click", function() {
  var newBook = {
    title: $("#title").val().trim(),
    author: $("#author").val().trim(),
    genre: $("#genre").val().trim()
  };
  $.post("/api/books", newBook, function() {
    // Reload the page to get the updated list of books
    location.reload();
  });
});

```

In this code snippet, we define the JavaScript logic for adding a new book. When the user clicks the "Add" button, we retrieve the values from the form fields and send a POST request to the `/api/books` API route with the new book data. We then reload the page to display the updated list of books.

6.  JavaScript logic for viewing data:

```javascript
$.get("/api/books", function(data) {
  for (var i = 0; i < data.length; i++) {
    var row = $("<tr>");
    row.append($("<td>").text(data[i].title));
    row.append($("<td>").text(data[i].author));
    row.append($("<td>").text(data[i].genre));
    $("#book-table").append(row);
  }
});

```

In this code snippet, we retrieve all books from the database by sending a GET request to the `/api/books` API route. We then loop through the data and create a new table row for each book, which we append to the `book-table` HTML table.

## Conclusion:

Through this exercise, you have learned how to use Sequelize, which is a powerful ORM for Node.js applications. You have learned how to set up a database connection, define Sequelize models, perform CRUD operations on the database, define and use API routes and HTML routes, and use JavaScript to interact with the API and HTML routes.