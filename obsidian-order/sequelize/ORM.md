# ORM

**ORM:** Object-relational-mapping is the idea of being able to write queries like the one above, as well as much more complicated ones, using the object-oriented paradigm of your preferred programming language.

**ORM:** According to Wikipedia an ORM is defined as a “technique for converting data between incompatible type systems using object-oriented programming languages”. Well, that does not give much detail into what they are capable of. So let us break it down into simpler terms.

-   An ORM allows us to interact with databases in the language that we prefer to code with.
    
-   It can also give you advanced features to help you manage and manipulate the information within your database.
    
-   The queries you create with an ORM can also perform better than a manual query written in the native language of the database.
    

But with all great things, there are always drawbacks that you must consider, such as:

-   The initial configuration of an ORM can be difficult.
    
-   There is additional learning that must be done to use any specific ORM.
    
-   It is also important to know exactly what your code is doing, and an ORM can make the commands it is executing more abstract therefore it can make a developer weaker in that part of the stack.
    

  
  

**ORM:**ORM (Object-Relational Mapping) is a technique that helps you to query and manipulate data from databases using an object-oriented paradigm. Nowadays developers like to use ORMs due to several reasons like,

-   Since we have to write a data model only in one place it is easier to update, maintain, and reuse the code.
    
-   Forces you to write [MVC](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller) code, which makes your code cleaner.
    
-   No need for writing SQL queries.
    
-   No need for database-level changes frequently.
    
-   Most of the work is automated.
    

But there are a few disadvantages of ORMs as well.

-   Performance issue with complex queries.
    
-   Integration and learning.

<hr>
ORM is a library to access the database, high-level library where you can define models, relations. Other option is to write pure SQL, and it's a valid option when performance is the biggest concern, but this way is not well suited for dynamic queries.

ORM is needed to make you more productive, to have automatically returned TS types instead of defining them each time by hand, to make it more safely so you can't accidentally pass dangerous string into SQL. Ideal ORM allows to define queries and then combine and reuse them to construct more complex queries.