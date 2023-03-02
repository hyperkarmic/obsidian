To complete the SQL code for this exercise, we need to add the missing column specifications to the `CREATE TABLE` statements and add a `DEFAULT` value for the `five_times` column in the `favorite_movies` table.

Here is the completed SQL code:

```sql
-- Drops the favorite_db if it exists currently --
DROP DATABASE IF EXISTS favorite_db;
-- Creates the "favorite_db" database --
CREATE DATABASE favorite_db;

-- Make it so all of the following code will affect favorite_db --

-- Creates the table "favorite_foods" within favorite_db --
CREATE TABLE favorite_foods (
  -- Make a string column called "food" which cannot contain null --
  food VARCHAR(50) NOT NULL,
  -- Make an numeric column called "score" --
  score INTEGER
);

CREATE TABLE favorite_songs (
  -- Make a string column called "song" which cannot contain null --
  song VARCHAR(100) NOT NULL,
  -- Make a string column called "artist" --
  artist VARCHAR(50),
  -- Make an integer column called "score" --
  score INTEGER
);

CREATE TABLE favorite_movies (
  -- Create a numeric column called "id" which automatically increments and cannot be null --
  id INT AUTO_INCREMENT PRIMARY KEY,
  -- Create a string column called "movie" which cannot be null --
  movie VARCHAR(255) NOT NULL,
  -- Create a boolean column called "five_times" that sets the default value to false if nothing is entered --
  five_times BOOLEAN DEFAULT false,
  -- Make an integer column called "score" --
  score INTEGER
);

```

To add data to a table, we can use the `INSERT INTO` statement. Here are some examples of how to insert data into the tables we just created:

```sql
-- Insert data into favorite_foods
INSERT INTO favorite_foods (food, score)
VALUES ('Pizza', 10);

-- Insert data into favorite_songs
INSERT INTO favorite_songs (song, artist, score)
VALUES ('Bohemian Rhapsody', 'Queen', 9);

-- Insert data into favorite_movies
INSERT INTO favorite_movies (movie, five_times, score)
VALUES ('The Dark Knight', true, 8);

```

The learning outcomes of this exercise include understanding how to create tables with specific columns and data types, setting primary keys, and inserting data into tables. The bonus question encourages learners to research further and expand their knowledge on SQL.

