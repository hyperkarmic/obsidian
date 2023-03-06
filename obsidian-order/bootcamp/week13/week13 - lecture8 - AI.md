First, make sure you have the necessary dependencies installed: Express, MySQL, and Handlebars. You can install them using npm:

```javascript
npm install express mysql handlebars

```

Next, create a file called `schema.sql` and add the following code to it:

```SQL
CREATE DATABASE wishes_db;

USE wishes_db;

CREATE TABLE wishes (
  id INT AUTO_INCREMENT PRIMARY KEY,
  wish VARCHAR(255)
);

```

This will create a database called `wishes_db` and a table called `wishes` with two columns: `id` and `wish`. The `id` column will be automatically incremented and set as the primary key.

Now, create a file called `server.js` and add the following code to it:

```javascript
const express = require('express');
const mysql = require('mysql');
const handlebars = require('express-handlebars');

const app = express();

// Set up handlebars
app.engine('handlebars', handlebars({ defaultLayout: 'main' }));
app.set('view engine', 'handlebars');

// Set up MySQL connection
const connection = mysql.createConnection({
  host: 'localhost',
  user: 'root',
  password: 'password',
  database: 'wishes_db'
});

// Connect to MySQL
connection.connect((err) => {
  if (err) throw err;
  console.log('Connected to MySQL');
});

// Set up routes
app.get('/', (req, res) => {
  // Retrieve all wishes from database
  connection.query('SELECT * FROM wishes', (err, results) => {
    if (err) throw err;

    // Render wishes using handlebars
    res.render('index', { wishes: results });
  });
});

app.post('/', (req, res) => {
  // Retrieve wish from form
  const wish = req.body.wish;

  // Insert wish into database
  connection.query('INSERT INTO wishes (wish) VALUES (?)', [wish], (err, results) => {
    if (err) throw err;

    // Redirect to home page
    res.redirect('/');
  });
});

// Start server
const PORT = process.env.PORT || 3000;
app.listen(PORT, () => {
  console.log(`Server started on port ${PORT}`);
});

```

This code sets up an Express app, connects to the MySQL database, and sets up two routes: a GET route for `'/'` and a POST route for `'/'`.

The GET route retrieves all wishes from the `wishes` table using the `SELECT` statement and renders them using Handlebars. The POST route retrieves the wish submitted through the form, inserts it into the `wishes` table using the `INSERT` statement, and then redirects the user back to the home page.

Note that this code assumes that you have a file called `index.handlebars` in a folder called `views` which renders the list of wishes and the form to add new wishes.

Learning outcomes from this code include:

-   Creating a MySQL database and table using SQL
-   Connecting to a MySQL database using the `mysql` module
-   Setting up routes in an Express app
-   Retrieving data from a MySQL database using the `SELECT` statement
-   Inserting data into a MySQL database using the `INSERT` statement
-   Using Handlebars to render dynamic content in an Express app.