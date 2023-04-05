This is an exercise focused on the use of Sequelize, which is an Object-Relational Mapping (ORM) library for Node.js that provides easy access to MySQL, MariaDB, PostgreSQL, SQLite, and Microsoft SQL Server databases.

The steps provided in the readme.md file guide developers through the process of converting an existing application that used ORM to Sequelize.

## Steps to Sequelize the Star Wars app

1.  Install the sequelize and mysql2 npm packages.
2.  Delete the orm from config. In your app folder, create a model folder with a character.js file in the model
3.  In character.js, model out the character table, as detailed in the schema.sql file located in the root of this project directory.
4.  Remove all references to the old orm file and replace it with character.js
5.  Use Sequelize methods in place of the orm calls to retrieve and insert data.
6.  Update connection.js to use sequelize instead of the mysql package.

## File Overview

### package.json

The package.json file lists all the packages required for the application to run, including express and mysql.

### server.js

The server.js file is the initial starting point for the Node/Express server.

### schema.sql

The schema.sql file contains SQL statements to create the `starwars` database and the `allcharacters` table.

### config/connection.js

The connection.js file sets up the database connection using the mysql package.

### config/orm.js

The orm.js file defines functions for accessing and manipulating the `allcharacters` table using SQL queries.

### routes/api-routes.js

The api-routes.js file contains the routes for the API endpoints used by the application.

### routes/html-routes.js

The html-routes.js file contains the routes for serving HTML pages.

### public/add.html, public/all.html, and public/view.html

The add.html, all.html, and view.html files are HTML pages served by the application.

### public/js/add.js, public/js/all.js, and public/js/view.js

The add.js, all.js, and view.js files contain client-side JavaScript code for the add, all, and view pages, respectively.

## Key Code Snippets

### Defining the Character Model (character.js)

The character model defines the `allcharacters` table, including its columns and data types, using Sequelize.

```javascript
module.exports = function(sequelize, DataTypes) {
  var Character = sequelize.define("Character", {
    routeName: {
      type: DataTypes.STRING,
      allowNull: false
    },
    name: {
      type: DataTypes.STRING,
      allowNull: false
    },
    role: {
      type: DataTypes.STRING,
      allowNull: false
    },
    age: {
      type: DataTypes.INTEGER,
      allowNull: false
    },
    forcePoints: {
      type: DataTypes.INTEGER,
      allowNull: false
    }
  });
  return Character;
};

```

### Retrieving All Characters (api-routes.js)

This code retrieves all characters from the `allcharacters` table using Sequelize's `findAll` method.

```javascript
app.get("/api/characters", function(req, res) {
  db.Character.findAll({}).then(function(result) {
    res.json(result);
  });
});

```


### Adding a New Character (api-routes.js)

This code adds a new character to the `allcharacters` table using Sequelize's `create` method.

```javascript
app.post("/api/characters", function(req, res) {
  var newCharacter = req.body;
  var routeName = newCharacter.name.replace(/\s+/g, "").toLowerCase();

  db.Character.create({
    routeName: routeName,
    name: newCharacter.name,
    role: newCharacter.role,
    age: newCharacter.age

```

***
How can TDD speed up coding?

-   Early detection of errors: When I code without writing tests, I make unpredictable mistakes (maybe I suck at writing code?) and I have to spend hours fixing them. Thanks to TDD, I can catch them early and save time. With TDD, you write automated tests before writing the actual code. This allows you to catch errors early before they have a chance to propagate and become more difficult to fix.
-   Happy refactoring: When you have a suite of automated tests, you can be confident that any refactoring you do to your codebase will not break existing functionality. This allows you to make changes to your codebase more quickly and with less fear of introducing bugs.
-   TDD forces us to think about the different scenarios and edge cases that our code may encounter later. Applying TDD, programmers anticipate potential issues early and can design their code more robustly. It saves time later.