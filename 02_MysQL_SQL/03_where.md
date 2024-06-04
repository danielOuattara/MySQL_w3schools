# MySQL WHERE Clause

##  The MySQL WHERE Clause

The `WHERE` clause is used to filter records.

It is used to extract only those records that fulfill a specified condition.

## WHERE Syntax

```sql
SELECT column1, column2, ...
    FROM table_name
    WHERE condition;
```

```text
Note: 
-----

The WHERE clause is not only used in SELECT statements, 
it is also used in UPDATE, DELETE, etc.!
```

## Demo Database

Below is a selection from the "Customers" table in the Northwind sample database:

##  WHERE Clause Example

> The following SQL statement selects all the customers from "Mexico":

```sql
SELECT * 
    FROM Customers
    WHERE Country = 'Mexico';
```

##  Text Fields vs. Numeric Fields

SQL requires single quotes around text values,
most database systems will also allow double quotes.

However, numeric fields should not be enclosed in quotes:

```sql
SELECT * 
    FROM Customers
    WHERE CustomerID = 1;
```

##  Operators in The WHERE Clause

| Operator | Description                                                      |
|:--------:|------------------------------------------------------------------|
|   =      | Equal to                                                         |
|   <      | Less than                                                        |
|   >      | Greater than                                                     |
|   >=     | Less than or equal to                                            |
|   >=     | Greater than or equal to                                         |
|   <>     | Not equal to                                                     |
|    !=    | Not equal to                                                     |
|   LIKE   | Check if a value matches a pattern (case sensitive)              |
|   ILIKE  | Check if a value matches a pattern (case    insensitive)         |
|    AND   | Logical AND                                                      |
|    OR    | Logical OR                                                       |
|    IN    | Check if a value is between a range of values                    |
|  BETWEEN | Check if a value is between a range of values                    |
|  IS NULL | Check if a value is NULL                                         |
|    NOT   | Makes a negative result e.g.    NOT LIKE, NOT IN,    NOT BETWEEN |
