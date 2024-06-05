# MySQL CREATE INDEX Statement

The `CREATE INDEX` statement is used to create
`indexes in tables`.

Indexes are used to retrieve data from the database
more quickly than otherwise.

The users cannot see the indexes, they are just used
to speed up searches/queries.

```text
Note: 
-----

Updating a table with indexes takes more time than updating 
a table without; because the indexes also need an update. 

So, only create indexes on columns that will be frequently 
searched against.
```

## CREATE INDEX Syntax

> Creates an index on a table. Duplicate values are allowed:

```sql
CREATE INDEX index_name
ON table_name (column1, column2, ...);
```

## CREATE UNIQUE INDEX Syntax

> Creates a unique index on a table. Duplicate values are not allowed:

```sql
CREATE UNIQUE INDEX index_name
ON table_name (column1, column2, ...);
```

## MySQL CREATE INDEX Example

The SQL statement below creates an index named `idx_lastname`
on the `LastName` column in the `Persons` table:

```sql
CREATE INDEX idx_lastname
ON Persons (LastName);
```

If you want to create an index on a combination of columns,
you can list the column names within the parentheses, separated
by commas:

```sql
CREATE INDEX idx_pname
ON Persons (LastName, FirstName);
```

## DROP INDEX Statement

The DROP INDEX statement is used to delete an index in a table.

```sql
ALTER TABLE table_name
DROP INDEX index_name;
```
