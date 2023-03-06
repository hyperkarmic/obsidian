The code represents a Node.js application that uses Express.js as a framework for creating a server that communicates with a MySQL database. The database contains a single table named "characters" with columns "id", "name", "coolness", and "attitude".

The `package.json` file lists the dependencies for the application, which are Express.js and MySQL packages. The `server.js` file defines the main functionality of the application, including the database configuration and initialisation, middleware definition, query and accessor methods, and routes definition. The `seed.sql` file contains SQL code to create the "characters" table and insert sample data.

The `server.js` file connects to the database on startup using the `mysql.createConnection` function with `dbOptions` object which contains the configuration details for the MySQL connection.

After connecting to the database, the middleware function `dbMiddleware` is declared and used in the Express application with the `app.use` function. The middleware function adds the database connection to the request object for use in the routes.

The `getAllAndOrderBy` method is defined to query the database for all records in the "characters" table ordered by the specified column using the `??` syntax for column names. The `getAllByAttitude` method is defined to query the database for all records in the "characters" table with a specific attitude.

The routes are then defined using `app.get` function, which listens for HTTP GET requests. The `/cast` route calls the `getAllAndOrderBy` method with the "id" column as the argument and returns the results in JSON format. The `/coolness-chart` route calls the `getAllAndOrderBy` method with the "coolness" column as the argument and returns the results in JSON format. The `/attitude-chart/:att` route calls the `getAllByAttitude` method with the specified attitude as the argument and returns the results in JSON format.

Finally, the application listens for incoming HTTP requests on the specified port using the `app.listen` function.

Learning Outcomes:

-   Understand how to use Express.js as a web framework for creating a server.
-   Understand how to connect to a MySQL database using the `mysql` package.
-   Understand how to use middleware functions to add functionality to an Express application.
-   Understand how to write queries to retrieve data from a MySQL database using the `mysql` package.
-   Understand how to define routes for an Express application using the `app.get` function.

***
This is a Node.js application that uses the Express framework and MySQL as the database. The application has three routes:

1.  `/cast` - displays all the actors and their data ordered by their id's.
2.  `/coolness-chart` - displays all the actors and their data ordered by their coolness points.
3.  `/attitude-chart/:att` - displays all the actors for a specific type of attitude.

The `server.js` file initializes the database connection and sets up middleware for handling database connections. It also defines three routes that utilize the accessor/query/repository methods to retrieve data from the database.

The `db/seed.sql` file contains the SQL commands for creating a new database `got_db` and a table `characters`. The table contains columns for `id`, `name`, `coolness`, and `attitude`. The SQL file also contains a command to insert data into the `characters` table.

The learning outcomes of this exercise include:

-   Understanding how to create a Node.js application with Express and MySQL.
-   Understanding how to create routes and middleware in an Express application.
-   Understanding how to execute SQL commands and retrieve data from a MySQL database in Node.js.
-   Understanding how to handle errors and use async/await in Node.js.

To run the application, you can use the following steps:

1.  Create a new directory for your project and navigate to it in your terminal.
2.  Create a new `package.json` file by running `npm init` and following the prompts.
3.  Install the necessary dependencies by running `npm install express mysql`.
4.  Create a new `src` directory and add a `server.js` file to it.
5.  Copy the code from the `server.js` file provided above into your `server.js` file.
6.  Create a new `db` directory and add a `seed.sql` file to it.
7.  Copy the SQL commands from the `seed.sql` file provided above into your `seed.sql` file.
8.  Run the SQL commands in your `seed.sql` file to create the database and insert data.
9.  Start the server by running `npm start` in your terminal.
10.  Test the routes by making requests to `http://localhost:3000/cast`, `http://localhost:3000/coolness-chart`, and `http://localhost:3000/attitude-chart/good` in your browser or using a tool like Postman.

***
The code provided is a Node.js application that uses Express and MySQL to display data from a database. It includes three routes that allow the user to query the database and retrieve information about the characters of Game of Thrones.

The package.json file includes information about the application and its dependencies, including Express and MySQL.

The server.js file is where the application logic is located. It begins by setting up a connection to the MySQL database using the database options specified in the file. It then declares a middleware function that will attach the database connection to the request object, allowing it to be used in subsequent middleware functions and routes.

The application has three routes: `/cast`, `/coolness-chart`, and `/attitude-chart/:att`. The `/cast` route retrieves all the characters from the database and orders them by their id. The `/coolness-chart` route retrieves all the characters from the database and orders them by their coolness points. The `/attitude-chart/:att` route retrieves all the characters from the database with a specific attitude.

The getAllAndOrderBy and getAllByAttitude methods are responsible for executing the appropriate database queries based on the route and user inputs. They use the promisify function from the util module to convert the callback-based MySQL API to a Promise-based API.

Finally, the application is started by calling the listen method on the express app object and specifying a port number.

To run the application, you will need to create a MySQL database and table using the seed.sql file provided in the db folder. Then, you can start the application by running `npm start` from the command line.

Learning outcomes from this code include understanding how to use Node.js with Express and MySQL to build a web application, understanding how to create middleware functions in Express, and understanding how to execute database queries asynchronously using Promises. Additionally, this exercise teaches how to create routes and handle user input.
***
This code exercise involves creating a Node.js application with Express.js and MySQL. The application should have three routes: `/cast`, `/coolness-chart`, and `/attitude-chart/:att`.

The `/cast` route displays all the actors and their data ordered by their id's. The `/coolness-chart` route displays all the actors and their data ordered by their coolness points. The `/attitude-chart/:att` route displays all the actors for a specific type of attitude.

The database schema and seed data are provided in the `db/seed.sql` file, and the database connection and query methods are defined in `src/server.js`.

To start the server, we can run the `start` script defined in the `package.json` file using the command `npm start`.

Here is an explanation of the key code snippets:

1.  Connecting to the database:

```javascript
const dbOptions = {
  host: "localhost",
  port: 3306,
  user: "root",
  password: "Manchester123",
  database: "got_db",
};

const connection = mysql.createConnection(dbOptions);

const onConnect = (err) => {
  if (err) throw err;
  console.log("Successfully connected to DB!!");
};

connection.connect(onConnect);

```

The code defines a configuration object for the database connection and initializes the connection using `mysql.createConnection()`. The `onConnect` function logs a success message when the connection is established.

2.  Middleware declaration:

```javascript
const dbMiddleware = (req, _, next) => {
  req.connection = connection;
  next();
};

app.use(dbMiddleware);

```

The code defines a middleware function that adds the database connection to the `req` object and calls `next()`. This middleware is used to provide access to the database connection in the route handlers.

3.  Query methods:

```javascript
const getAllAndOrderBy = async (req, orderBy) => {
  const queryAsync = promisify(req.connection.query).bind(req.connection);

  try {
    const result = await queryAsync(
      "SELECT * FROM characters ORDER BY ?? ASC",
      orderBy
    );

    return result;
  } catch (err) {
    console.error(err);
  }
};

const getAllByAttitude = async (req, attitude) => {
  const queryAsync = promisify(req.connection.query).bind(req.connection);

  try {
    const result = await queryAsync(
      "SELECT * FROM characters WHERE attitude=?",
      attitude
    );

    return result;
  } catch (err) {
    console.error(err);
  }
};

```

The code defines two query methods that are used in the route handlers. `getAllAndOrderBy()` retrieves all characters from the database and orders them by a specified column. `getAllByAttitude()` retrieves all characters from the database that have a specified attitude.

4.  Route handlers:

```javascript
app.get("/cast", async (req, res) => {
  const characters = await getAllAndOrderBy(req, "id");

  res.json({
    characters,
  });
});

app.get("/coolness-chart", async (req, res) => {
  const characters = await getAllAndOrderBy(req, "coolness");

  res.json({
    characters,
  });
});

app.get("/attitude-chart/:att", async (req, res) => {
  const characters = await getAllByAttitude(req, req.params.att);

  res.json({
    characters,
  });
});

```

The code defines three route handlers for the `/cast`, `/coolness-chart`, and `/attitude-chart/:att` routes. Each route handler calls a query method to retrieve data from the database and returns the result as a JSON object using `res.json()`.

5.  Starting the server: