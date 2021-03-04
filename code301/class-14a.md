# Database Normalization -[Kris Wenzel](https://www.essentialsql.com/get-ready-to-learn-sql-database-normalization-explained-in-simple-english/)

Dtatbase normalization is the procees of organizing a database with the idea of compartmentalizing the data to contain specific relational data. This makes the data more serachable, eliminates redundant data and the database easier to use and modify over time.

There are three normal forms most databases adhere to using:

- **First Normal Form**: The information is stored in a relational tabble with each column containing atomic values. There are no repeating groups of columns.

- **Second Normal Form**: The table is in first normal form and all the columns depend on the table's primary key.

- **Third Normal Form**: The table is in the second normal form and all of it columns are not transitively dependent on the primary key.

