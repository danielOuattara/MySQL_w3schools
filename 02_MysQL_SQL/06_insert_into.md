#  MySQL INSERT INTO Statement

##  The MySQL INSERT INTO Statement

The `INSERT INTO` statement is used to insert new
records in a table.

### INSERT INTO Syntax

It is possible to write the INSERT INTO statement in two ways:

1. Specify both the column names and the values to be inserted:

```sql
INSERT INTO 
    table_name (column1, column2, column3, ...)
VALUES 
    (value1, value2, value3, ...);
```

2. If you are adding values for all the columns of the table,
   you do not need to specify the column names in the SQL query.

   However, make sure the order of the values is in the same order
   as the columns in the table.
   Here, the INSERT INTO syntax would be as follows:

```sql
INSERT INTO 
    table_name
VALUES 
    (value1, value2, value3, ...);
```

## INSERT INTO Example

The following SQL statement inserts a new record in the "Customers" table:

```SQL
INSERT INTO  
    customers (customer_name, contact_name, address, city, postal_code, country)
VALUES 
    ('Cardinal', 'Tom B. Erichsen', 'Skagen 21', 'Stavanger', '4006', 'Norway');
```

> **NOTE**
>
> Did you notice that we did not insert any number into the CustomerID field?
>
> The `id` column is an auto-increment field and will be generated automatically
> when a new record is inserted into the table.

## Insert Data Only in Specified Columns

It is also possible to only insert data in specific columns.

The following SQL statement will insert a new record, but only insert data
in the "CustomerName", "City", and "Country" columns (CustomerID will be
updated automatically):

```sql
INSERT INTO 
    customers (customer_name, city, country)
VALUES 
    ('Cardinal', 'Stavanger', 'Norway');
```
