# Relational Database
What’s the structure of a relational database model?

A relational database is a type of database organized expressly to recognize connections between different informational items — types of “relational data.” It was invented in 1970 by an IBM programmer named E.F. Codd.

More fluid than a hierarchical database, the database design is made up of different tables that can be mixed and matched, put together in various ways, to enable users to easily locate exactly the data points they’re looking for in order to be able to get all the details they need at once, make correlations, and draw conclusions. 

Each table in a relational database includes: 

-   Columns of categories
-   Rows (also known as tuples or records)

The rows are where the unique data is stored, and each table has a “primary key” to define its information. So for example, to store information for an everyday purchase order, a primary key column might be tagged Customer, with columns for categories such as Name, Contact Details, and Date. Alongside this might be an “Order Number” primary key with columns for Customer, Product, Price, and other details.

***
## **The structure of a relational database** 

Relational databases are structured using [Structured Query Language (SQL)](https://www.algolia.com/doc/guides/sending-and-managing-data/prepare-your-data/in-depth/prepare-data-in-depth/), which enables users to query it to bring together the bits of information they need. 

When first devised, the relational database model was a departure from IBM’s previously hierarchical structures, which required users to navigate through a “treelike” design with multiple “branches” to retrieve desired information. 

## **How a hierarchical database works**

In a hierarchical database, the same data is required to be repetitively stored in multiple places, which makes searching for specific information in near real time and seeing how certain data relates to each other more difficult. To find needed information, you’d have to search the entire model from top to bottom. And in a modern workplace where the volume of data is increasing all the time, making connections and drawing insights from that data is almost impossible. 

A good example of a hierarchical database is one most people have seen at some point: an organizational ladder chart. The information is stored based on fundamental elements (items such as tables, records, and fields).

-   At the top of the hierarchy is the CEO or founder
-   A rung below that are the department heads or team leads
-   Below this level are the members of the leaders’ teams
***
