# joins
***
The SQL Join clause is used to combine records (rows) from two or more tables in a SQL database based on a related column between the two.

![[joins.png]]
There are four different types of JOINs in SQL:

(INNER) JOIN: Retrieves records that have matching values in both tables involved in the join. This is the widely used join for queries.

LEFT (OUTER) JOIN: Retrieves all the records/rows from the left and the matched records/rows from the right table.

RIGHT (OUTER) JOIN: Retrieves all the records/rows from the right and the matched records/rows from the left table.

FULL (OUTER) JOIN: Retrieves all the records where there is a match in either the left or right table.

1.  What is a Self-Join? A self JOIN is a case of regular join where a table is joined to itself based on some relation between its own column(s). Self-join uses the INNER JOIN or LEFT JOIN clause and a table alias is used to assign different names to the table within the query.
***
![[sql_join.jpg]]
***
![[sql_joins_syntax.jpg]]
![[sql-join-brown.jpg]]

#joins #SQL