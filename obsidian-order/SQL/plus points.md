# SQL Good
1.  **Relational databases are not so easy to scale.** I am not saying they can’t. Facebook uses relational databases. So they can scale. But it’s a bit challenging for the architects to do it.
2.  Here’s a [_case study_](https://www.notion.so/blog/sharding-postgres-at-notion) of Notion and how they sharded their databases as they expanded.
3.  **Relational databases are not very good where the amount of data is varying.** Let’s take the example of a model where you need to store details of a candidate applying for a job.
4.  A candidate might have worked at 10 different companies or maybe just 1. Or they could have gone to 2 schools and 0 universities but might have done great courses on Udemy. Such data is not quite ideal to have a schema attached to it, hence not so suitable for relational databases.
5.  Also, if the data has too many types then it’s not ideal to create tables for each type since joins will induce their own write and read overheads.
6.  **Having a schema can be limiting.** Relational DBs have constraints tied to them. For e.g. if two tables have a foreign key relationship, deleting a row in one table will delete the associated row in the related table.
7.  So it’s useful in cases where the data needs to be rigid, but you will have to take care of such corner cases.
8.  **Multilevel joins can slow down your queries.** When you query multiple tables for information, you create joins. When you have multi-level joins like this, it becomes slower and slower to query. If your APIs are getting slower, check the SQL queries and you may understand why.
#SQL #bad
