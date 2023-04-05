The aim of this exercise is to use Sequelize ORM library to create and read data from a database. The task is to create two routes, one that retrieves all the todos from the database, and another that creates a new todo and saves it to the database.

Project structure:

The project has a server.js file that serves as the entry point for the application. The code for handling routes is located in the routes folder in the api-routes.js file. The models folder has two files: index.js and todo.js. The index.js file sets up the association between the models, and the todo.js file defines the Todo model. The public folder contains the client-side code, including the HTML, CSS, and JavaScript files.

Instructions:

1.  Install the required dependencies by running `npm install` in the project directory.
    
2.  Update the `config.json` file with your own local MYSQL database settings.
    
3.  Inside the `api-routes.js` file, add a Sequelize `findAll` method inside the GET route, which finds all the todos and returns them to the user as JSON.

```javascript
app.get("/api/todos", function(req, res) {
  db.Todo.findAll({}).then(function(dbTodos) {
    res.json(dbTodos);
  });
});

```

Add a Sequelize `create` method to the POST route, which saves a new todo to the database using the data sent to the server in `req.body`.

```javascript
app.post("/api/todos", function(req, res) {
  db.Todo.create({
    text: req.body.text,
    complete: req.body.complete
  }).then(function(dbTodo) {
    res.json(dbTodo);
  });
});

```

1.  To test if everything works, open your terminal and run `node server` and navigate to localhost:8080. If you are able to save new todos, you were successful.
    

Learning outcomes:

Through this exercise, you will learn how to use Sequelize ORM library to create and read data from a database. Specifically, you will learn:

-   How to define a Sequelize model for a database table.
-   How to use Sequelize to find all records in a table.
-   How to use Sequelize to create new records in a table.

