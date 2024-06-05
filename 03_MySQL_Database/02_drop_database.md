# MySQL DROP DATABASE Statement

##  The MySQL DROP DATABASE Statement

The `DROP DATABASE` statement is used to drop
an existing SQL database.

##  Syntax

```sql
DROP DATABASE database_name;
```

```text
Note: 
-----

Be careful before dropping a database. 
Deleting a database will result in loss of complete 
information stored in the database!
```

##  DROP DATABASE Example

> The following SQL statement drops the existing database "testDB":

```sql
DROP DATABASE testDB;
```

```text

Tip: 
----

Make sure you have admin privilege before dropping any database. 
Once a database is dropped, you can check it in the list of 
databases with the following SQL command: 

SHOW DATABASES;
```
