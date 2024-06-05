#  MySQL DROP TABLE Statement

##  The MySQL DROP TABLE Statement

The `DROP TABLE` statement is used to drop an existing
table from a database.

##  Syntax

```sql
DROP TABLE table_name;
```

```text
Note: 
-----

Be careful before dropping a table: deleting a table 
will result in loss of complete information stored in 
the table!
```

##  MySQL DROP TABLE Example

> The following SQL statement drops the existing table
> "Shippers":

```sql
DROP TABLE Shippers;
```

## MySQL TRUNCATE TABLE

The `TRUNCATE TABLE` statement is used to delete the
data inside a table, but not the table itself.

### Syntax

```sql
TRUNCATE TABLE table_name;
```
