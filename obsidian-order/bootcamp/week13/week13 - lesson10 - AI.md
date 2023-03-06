To complete the requirements outlined in the readme.md file, we will need to do the following:

1.  Create a `package.json` file using `npm init`.
2.  Install the required dependencies, including Express, Handlebars, MySQL, and nodemon, using `npm install express handlebars mysql nodemon`.
3.  Create a `schema.sql` file and add the necessary SQL commands to create the `moviePlannerDB` database and the `movies` table.
4.  Create a `connection.js` file to establish a connection to the MySQL database.
5.  Create a `orm.js` file to define the object-relational mapping for the `movies` table.
6.  Create a `moviesController.js` file to define the routes for the application.
7.  Create an `index.handlebars` file to render the main page of the application.
8.  Create a `add-movie.handlebars` file to render the form to add a movie to the database.
9.  Create an `update-movie.handlebars` file to render the form to update a movie in the database.

### 1. Create a `package.json` file

We will start by creating a `package.json` file using `npm init`. This file will store information about the project, such as its name, version, description, and dependencies.

To create the `package.json` file, we can run the following command in the terminal:

```javascript
npm init

```

### 2. Install the required dependencies

Next, we will install the required dependencies using `npm install express handlebars mysql nodemon`.

The `express` package is a popular Node.js framework for building web applications. We will use it to handle HTTP requests and responses.

The `handlebars` package is a templating engine that allows us to create reusable views for our web application.

The `mysql` package is a Node.js driver for MySQL that allows us to interact with the MySQL database.

The `nodemon` package is a tool that automatically restarts the server when changes are made to the code. This will save us time and make the development process faster.

We can install these packages by running the following command:

```javascript
npm install express handlebars mysql nodemon

```

### 3. Create a `schema.sql` file

Next, we will create a `schema.sql` file and add the necessary SQL commands to create the `moviePlannerDB` database and the `movies` table.

Here's what the `schema.sql` file should look like:

```SQL
-- Create the moviePlannerDB database
CREATE DATABASE IF NOT EXISTS moviePlannerDB;

-- Use the moviePlannerDB database
USE moviePlannerDB;

-- Create the movies table
CREATE TABLE IF NOT EXISTS movies (
  id INT NOT NULL AUTO_INCREMENT,
  movie VARCHAR(255) NOT NULL,
  PRIMARY KEY (id)
);

```

### 4. Create a `connection.js` file

Next, we will create a `connection.js` file to establish a connection to the MySQL database.

Here's what the `connection.js` file should look like:

```javascript
const mysql = require('mysql');

// Create a connection to the database
const connection = mysql.createConnection({
  host: 'localhost',
  port: 3306,
  user: 'root',
  password: 'password',
  database: 'moviePlannerDB',
});

// Connect to the database
connection.connect((err) => {
  if (err) {
    console.error(`Error connecting to the database: ${err.stack}`);
    return;
  }

  console.log(`Connected to the database with ID ${connection.threadId}`);
});

// Export the connection for ORM use
module.exports = connection;

```

***
To complete the requirements of the `readme.md` file, we need to create the following files:

1.  `schema.sql` file to create a database and a movies table inside that database.
2.  `server.js` file to create four routes (`get`, `post`, `put`, and `delete`) and render `index.handlebars` template on the `'/'` route, as well as handle create, update, and delete operations on the movies table.

Let's create the `schema.sql` file first. In the root directory of our project, create a new file called `schema.sql`. Inside this file, write the following code:

```SQL
CREATE DATABASE IF NOT EXISTS moviePlannerDB;
USE moviePlannerDB;

CREATE TABLE IF NOT EXISTS movies (
  id INT AUTO_INCREMENT PRIMARY KEY,
  movie VARCHAR(255) NOT NULL
);

```

This code creates a database called `moviePlannerDB` if it does not already exist, and creates a table called `movies` with two columns: `id` and `movie`. The `id` column is set to be the primary key and will automatically increment with each new record inserted into the table.

Next, let's create the `server.js` file. In the root directory of our project, create a new file called `server.js`. Inside this file, write the following code:

```javascript
// Dependencies
const express = require('express');
const mysql = require('mysql');
const exphbs = require('express-handlebars');

// Set up the Express app
const app = express();
const PORT = process.env.PORT || 8080;

// Set up the MySQL connection
const connection = mysql.createConnection({
  host: 'localhost',
  user: 'root',
  password: 'password',
  database: 'moviePlannerDB'
});

// Connect to the MySQL server
connection.connect((err) => {
  if (err) {
    console.error(`Error connecting to MySQL: ${err.stack}`);
    return;
  }
  console.log(`Connected to MySQL as id ${connection.threadId}`);
});

// Set up the Handlebars engine
app.engine('handlebars', exphbs({ defaultLayout: 'main' }));
app.set('view engine', 'handlebars');

// Set up the Express app to handle data parsing
app.use(express.urlencoded({ extended: true }));
app.use(express.json());

// Create a route to get all movies from the movies table
app.get('/', (req, res) => {
  const sql = 'SELECT * FROM movies';
  connection.query(sql, (err, results) => {
    if (err) throw err;
    res.render('index', { movies: results });
  });
});

// Create a route to add a new movie to the movies table
app.post('/movies', (req, res) => {
  const movie = req.body.movie;
  const sql = 'INSERT INTO movies (movie) VALUES (?)';
  connection.query(sql, [movie], (err, result) => {
    if (err) throw err;
    res.json({ id: result.insertId });
  });
});

// Create a route to update a movie in the movies table
app.put('/movies/:id', (req, res) => {
  const id = req.params.id;
  const movie = req.body.movie;
  const sql = 'UPDATE movies SET movie = ? WHERE id = ?';
  connection.query(sql, [movie, id], (err, result) => {
    if (err) throw err;
    res.json({ success: true });
  });
});

// Create a route to delete a movie from the movies table
app.delete('/movies/:id', (req, res) => {
  const id = req.params

```

***
To complete the requirements outlined in the `readme.md` file, we will need to create the following files:

1.  `schema.sql` file: This file will contain the SQL commands required to create the `moviePlannerDB` database and the `movies` table with columns `id` and `movie`.
    
2.  `server.js` file: This file will contain the JavaScript code for creating four routes: `get`, `post`, `put`, and `delete`. The `get` route will render the `index.handlebars` template with all of the movies from the `movies` table. The `/movies` route will have three operations: create, update, and delete. The create operation will insert a new movie into the `movies` table and return the ID of the new movie. The update operation will update an existing movie in the `movies` table. The delete operation will delete a movie from the `movies` table.
    
3.  `index.handlebars` file: This file will contain the HTML code for rendering the main page of the web application.
    

Let's start by creating the `schema.sql` file.

schema.sql

```SQL
-- create moviePlannerDB database
CREATE DATABASE IF NOT EXISTS moviePlannerDB;

-- use moviePlannerDB database
USE moviePlannerDB;

-- create movies table
CREATE TABLE IF NOT EXISTS movies (
  id INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
  movie VARCHAR(255) NOT NULL
);

```

The `schema.sql` file contains the SQL commands to create the `moviePlannerDB` database and the `movies` table with two columns: `id` and `movie`. The `id` column is an auto-incrementing integer and the primary key for the table. The `movie` column is a string that cannot be null.

Next, let's create the `server.js` file.

server.js

``` javascript
const express = require('express');
const mysql = require('mysql');
const exphbs = require('express-handlebars');

const app = express();

// set up the Express app to handle data parsing
app.use(express.urlencoded({ extended: true }));
app.use(express.json());

// set up handlebars as the view engine
app.engine('handlebars', exphbs({ defaultLayout: 'main' }));
app.set('view engine', 'handlebars');

// create a connection to the MySQL database
const connection = mysql.createConnection({
  host: 'localhost',
  port: 3306,
  user: 'root',
  password: '',
  database: 'moviePlannerDB',
});

// connect to the MySQL database
connection.connect((err) => {
  if (err) {
    console.error(`error connecting to the database: ${err.stack}`);
    return;
  }
  console.log(`connected to the database with id ${connection.threadId}`);
});

// GET route to render the main page with all movies from the movies table
app.get('/', (req, res) => {
  connection.query('SELECT * FROM movies', (err, data) => {
    if (err) throw err;

    res.render('index', { movies: data });
  });
});

// POST route to add a new movie to the movies table
app.post('/movies', (req, res) => {
  const movie = req.body.movie;

  connection.query('INSERT INTO movies SET ?', { movie }, (err, data) => {
    if (err) throw err;

    res.json({ id: data.insertId });
  });
});

// PUT route to update an existing movie in the movies table
app.put('/movies/:id', (req, res) => {
  const id = req.params.id;
  const movie = req.body.movie;


```