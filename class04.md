# PostgreSQL Joins

1. Inner Join creates a table with rows that match the joined column values
2. Left  Join adds the second table values if the column matches and includes all the first table values
3. Right Join is the opposite of Left Join
4. Full Outer Join adds a row if either table has a matching value

* one to one

- A one to one relationship is when a row can be linked with only one row in another table and vice versa. 

* one to many

- A one to many relationship is when a row in a table can be linked with many rows in another table, but that row is linked to other tables, like an author can have many books, but each book has only one author

* many to many

- A many to many relationship is when multiple rows in a table can be linked with multiple rows in another table, like people who build lego sets. Each lego set can be built by different people, and different people can each build different lego sets.