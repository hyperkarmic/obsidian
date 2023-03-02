This .sql file creates a database called "books_db" and two tables: "books" and "authors". It then inserts some sample data into the tables and performs three SELECT statements with JOINs to demonstrate how to combine data from the two tables.

Here are the key code snippets and explanations:

1.  Creating the "books" table:

```sql CREATE TABLE books(
  id INTEGER(11) AUTO_INCREMENT NOT NULL,
  authorId INTEGER(11),
  title VARCHAR(100),
  PRIMARY KEY (id)
);


```

This code creates a table called "books" with three columns: "id", "authorId", and "title". The "id" column is a primary key with auto-increment enabled. The "authorId" column is a foreign key referencing the "id" column of the "authors" table.

2.  Creating the "authors" table:

```sql
CREATE TABLE authors(
  id INTEGER(11) AUTO_INCREMENT NOT NULL,
  firstName VARCHAR(100),
  lastName VARCHAR(100),
  PRIMARY KEY (id)
);

```

This code creates a table called "authors" with three columns: "id", "firstName", and "lastName". The "id" column is a primary key with auto-increment enabled.

3.  Inserting data into the "authors" table:

```sql
INSERT INTO authors (firstName, lastName) values ('Jane', 'Austen');
INSERT INTO authors (firstName, lastName) values ('Mark', 'Twain');
INSERT INTO authors (firstName, lastName) values ('Lewis', 'Carroll');
INSERT INTO authors (firstName, lastName) values ('Andre', 'Asselin');

```

These codes insert four rows into the "authors" table.

4.  Inserting data into the "books" table:

```sql
INSERT INTO books (title, authorId) values ('Pride and Prejudice', 1);
INSERT INTO books (title, authorId) values ('Emma', 1);
INSERT INTO books (title, authorId) values ('The Adventures of Tom Sawyer', 2);
INSERT INTO books (title, authorId) values ('Adventures of Huckleberry Finn', 2);
INSERT INTO books (title, authorId) values ('Alice''s Adventures in Wonderland', 3);
INSERT INTO books (title, authorId) values ('Dracula', null);

```

These codes insert six rows into the "books" table. Note that the last row has a null value for the "authorId" column.

5.  SELECT statement with INNER JOIN:

```sql
SELECT title, firstName, lastName
FROM books
INNER JOIN authors ON books.authorId = authors.id;

```

This code selects all rows from the "books" table and their corresponding authors' first and last names. The INNER JOIN keyword is used to combine the data from the two tables based on the matching "id" values in the "books" and "authors" tables.

6.  SELECT statement with LEFT JOIN:

```sql
SELECT title, firstName, lastName
FROM books
LEFT JOIN authors ON books.authorId = authors.id;

```

This code selects all rows from the "books" table and their corresponding authors' first and last names, even if the author information is missing. The LEFT JOIN keyword is used to combine the data from the two tables and include all rows from the "books" table and their matching rows from the "authors" table.

7.  SELECT statement with RIGHT JOIN:

```sql
SELECT title, firstName, lastName
FROM books
RIGHT JOIN authors ON books.authorId = authors.id;

```

This code selects all rows from the "authors" table and their corresponding books' titles, even if the book information is missing. The RIGHT JOIN keyword is used to combine the data from the two tables