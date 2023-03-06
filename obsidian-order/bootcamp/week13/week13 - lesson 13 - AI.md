The exercise involves creating a holiday party planner application that helps in creating parties for clients while keeping track of all the events being hosted. The application uses Node.js and MySQL to create and connect to a database called `parties_db`. The database has two tables- `clients` and `parties` with the appropriate columns. `schema.sql` is used to create the database and tables, while `seeds.sql` is used to seed the initial values.

The application uses an ORM to perform queries on the database. The ORM is created in the `orm.js` file and has the following functionalities:

-   Console log all the party names.
-   Console log all the client names.
-   Console log all the parties that have a party-type of grown-up.
-   Console log all the clients and their parties.

Learning Outcomes: This exercise helps in understanding the following concepts:

-   Creating a MySQL database and tables using `schema.sql`.
-   Seeding initial values using `seeds.sql`.
-   Connecting to MySQL database using Node.js and `connection.js`.
-   Creating an ORM and performing queries on the database using Node.js and MySQL.

Code: Below are the key code snippets for this exercise:

### schema.sql

```sql
CREATE DATABASE parties_db;

USE parties_db;

CREATE TABLE clients
(
	id int NOT NULL AUTO_INCREMENT,
	client_name varchar(255) NOT NULL,
	PRIMARY KEY (id)
);

CREATE TABLE parties
(
	id int NOT NULL AUTO_INCREMENT,
	party_name varchar(255) NOT NULL,
	party_type varchar(255) NOT NULL,
	party_cost int NOT NULL,
	client_id int NOT NULL,
	PRIMARY KEY (id),
	FOREIGN KEY (client_id) REFERENCES clients(id)
);

```

The `schema.sql` file creates the `parties_db` database and two tables- `clients` and `parties`.

### seeds.sql

```sql
INSERT INTO clients (client_name) VALUES ('Bilal');
INSERT INTO clients (client_name) VALUES ('Brianne');
INSERT INTO clients (client_name) VALUES ('Vincent');

INSERT INTO parties (party_name, party_type, party_cost, client_id) VALUES ('Everybody Loves Raymond', 'tv', 500, 1);
INSERT INTO parties (party_name, party_type, party_cost, client_id) VALUES ('Big Bang Theory', 'tv', 900, 1);
INSERT INTO parties (party_name, party_type, party_cost, client_id) VALUES ('Top Gun', 'movie', 200, 2);
INSERT INTO parties (party_name, party_type, party_cost, client_id) VALUES ('Whiskey', 'grown-up', 300, 2);
INSERT INTO parties (party_name, party_type, party_cost, client_id) VALUES ('Cigar', 'grown-up', 250, 3);

```

The `seeds.sql` file seeds the initial values for the `clients` and `parties` tables.

### connection.js

```javascript
const mysql = require('mysql');

const connection = mysql.createConnection({
  host: 'localhost',
  port: 3306,
  user: 'root',
  password: 'password',
  database: 'parties_db',
});

connection.connect((err) => {
  if (err) throw err;
  console.log(`Connected as id ${connection.threadId}`);
});

module.exports = connection;

```

The `connection.js` file creates a connection to the MySQL database `parties_db` using the `mysql` npm package.

### orm.js

```javascript
const connection = require('./config/connection');

const orm = {
  getAllParties() {
    const query = `
      SELECT *
      FROM parties
    `;
    connection.query(query, (err, res) => {

```