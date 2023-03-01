This is a basic application that demonstrates the use of Node.js and Express.js, with jQuery. The purpose of the app is to help schedule reservation requests for a restaurant that has only five tables available. The first five requests get a reservation, and every request after that is sent to the waiting list. The application has the following files:

-   `readme.md`: Provides an overview of the application and its purpose.
-   `phases.md`: Provides information on the app, as well as instructions on how to use it.
-   `src/data/tables.json`: Contains data on the current reservations and waiting lists.
-   `src/server/index.js`: Contains the main code for the application, which includes middleware functions, utility functions, and routes.
-   `src/views/index.html`: Contains the HTML code for the index page.
-   `src/views/tables.html`: Contains the HTML code for the tables page.
-   `src/views/reservation.html`: Contains the HTML code for the reservation page.
-   `server.js`: The main entry point for the application.
-   `data.json`: Contains the data for the current reservations and waiting lists.
-   `package.json`: Contains metadata and dependencies for the application.

## Key code snippets

### Middleware

The following code sets up middleware for the application, which includes parsing incoming requests and responses:

```javascript
// Middleware
app.use(express.urlencoded({ extended: true }));
app.use(express.json());

```

### Utility functions

The following code defines utility functions for the application, which include functions to read and write data from the `tables.json` file:

```javascript
const readFileAsync = promisify(fs.readFile);
const writeFileAsync = promisify(fs.writeFile);

const getTablesFromFile = async () => {
  const filePath = path.join(__dirname, "../data/tables.json");
  const tablesData = await readFileAsync(filePath, "utf8");
  const tables = JSON.parse(tablesData);
  return tables;
};

const writeTablesToFile = async (tables) => {
  const filePath = path.join(__dirname, "../data/tables.json");
  await writeFileAsync(filePath, JSON.stringify(tables));
};

```

### Routes

The following code defines the routes for the application:

```javascript
// ROUTES
app.get("/", serveIndexFile);
app.get("/tables", serveTablesFile);
app.get("/reserve", serveReserveFile);
app.get("/api/tables", getTables);
app.get("/api/waitingTables", getWaitingTables);
app.post("/api/reserve", createReservations);
app.delete("/api/tables", deleteTables);

```

The routes include `serveIndexFile()`, `serveTablesFile()`, and `serveReserveFile()`, which serve the HTML files for the index, tables, and reservation pages, respectively. The routes also include `getTables()`, `getWaitingTables()`, `createReservations()`, and `deleteTables()`, which handle getting the current tables and waiting lists, creating a new reservation, and deleting all reservations, respectively.

### Server setup

The following code sets up the server for the application:

```javascript
app.listen(PORT, () => {
  console.log(`Server listening on: http://localhost:${PORT}`);
});

```

This code listens for incoming requests on port 3000 and logs a message to the console when the server starts.

## Learning outcomes

By working with this application, developers can learn how to:

-   Build a basic web application using Node.js and Express.js
-   Implement middleware to handle incoming requests and responses
-   Set up routes for handling different types of requests
-   Use utility functions to read and write data to files
-   Implement client-side functionality using jQuery