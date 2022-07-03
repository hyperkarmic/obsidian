# schema
Schema: Schemas define the structure of data/document.

**Schema** (aka: data model) is a metadata describing the data type, formats, and validation rules. Schema can be defined for content body, header, path or query parameters, etc.

Schema:A database schema is an abstract design that represents the storage of your data in a database

Schema:A database schema ia ****blueprint**** or ****architecture**** of how our data will look. It doesn’t hold data itself, but instead describes the shape of the data and how it might relate to other tables or models. An entry in our database will be an instance of the database schema. It will contain all of the properties described in the schema.

_Think of a database schema as a type of data structure. It represents the framework and arrangement of the contents of an organization’s data._
***
## What Is a Database Schema?

That’s actually a bit of a difficult question to answer! Like many database terms, _database schema_ gets used in a variety of contexts. Depending on the context, it can mean different things.

In the context of generally discussing a database and how it’s organized, the term database schema describes the structure of the data and how the elements within the database relate to each other. This information is often presented visually with diagrams that illustrate how different tables and elements connect to give you a logical view of the entire database. However, the schema itself exists _in_ the database as the coded rules that define the data’s structure and relationships.

In this context, the database schema is typically something that’s typically planned prior to the creation of a new database. It reflects the design of your database, and it’s always best to design _before_ you start building! An architect or developer considers what is required based on the data model or application, and then makes decisions about the tables, data types, foreign key constraints, etc. that will be included. The resulting design is called the database schema.

To sum up, a _database schema_:

-   Defines how data in a database is structured
-   Defines how elements within a database relate to each other
-   Accomplishes the above through the implementation of coded rules

In this article, we’ll focus primarily on the above definition of database schema, as architects and developers must think carefully about their schema design prior to creating and implementing a database. But first, to avoid confusion we need to understand a few other ways the term _database schema_ gets used.
***


## Other Definitions of “Database Schema”

In SQL databases, the term _database schema_ can also have another, more specific meaning. The term “schema” is sometimes used to represent a named group of database objects. This type of schema is more precisely called _user-defined schema_, so to avoid confusion, we’ll use that term for the remainder of this article.
***
![[schema.png]]
***
![[schema vs model.png]]
***

#schema
#database
#SQL 