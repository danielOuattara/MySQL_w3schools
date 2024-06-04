# MySQL: AND, OR and NOT Operators

## The MySQL AND, OR and NOT Operators

The `WHERE` clause can be combined with `AND`, `OR`, and
`NOT` operators.

The `AND` and `OR` operators are used to filter records based
on more than one condition:

- The `AND` operator displays a record if all the conditions
  separated by `AND` are `TRUE`.

- The `OR` operator displays a record if any of the conditions
  separated by`OR` is `TRUE`.

The `NOT` operator displays a record if the condition(s)
`is NOT TRUE`

##  AND Syntax

```sql
SELECT column1, column2, ...
    FROM table_name
    WHERE condition1 AND condition2 AND condition3 ...;
```

##  OR Syntax

```sql
SELECT column1, column2, ...
    FROM table_name
    WHERE condition1 OR condition2 OR condition3 ...;
```

## NOT Syntax

```sql
SELECT column1, column2, ...
    FROM table_name
    WHERE NOT condition;
```

##  Demo Database

The table below shows the complete `Customers` table from
the Northwind sample database:

## AND Example

> The following SQL statement selects all fields from `Customers`
> where country is `Germany` AND city is `Berlin`:

```sql
SELECT * 
    FROM Customers
    WHERE Country = 'Germany' AND City = 'Berlin';
```

##  OR Example

> The following SQL statement selects all fields from `Customers`
> where city is `Berlin` OR `Stuttgart`:

```sql
SELECT * 
    FROM Customers
    WHERE City = 'Berlin' OR City = 'Stuttgart';
```

> The following SQL statement selects all fields from `Customers`
> where country is `Germany` OR `Spain`:

```sql
SELECT * 
    FROM Customers
    WHERE Country = 'Germany' OR Country = 'Spain';
```

## NOT Example

> The following SQL statement selects all fields from `Customers`
> where country is NOT `Germany`:

```sql
SELECT * 
    FROM Customers
    WHERE NOT Country = 'Germany';
```

##  Combining AND, OR and NOT

You can also combine the AND, OR and NOT operators.

> The following SQL statement selects all fields from `Customers`
> where country is `Germany` AND city must be `Berlin` OR `Stuttgart`
> (use parenthesis to form complex expressions):

```sql
SELECT * 
    FROM Customers
    WHERE Country = 'Germany' AND (City = 'Berlin' OR City = 'Stuttgart');
```

> The following SQL statement selects all fields from `Customers`
> where country is NOT `Germany` and NOT `USA`:

```sql
SELECT * 
    FROM Customers
    WHERE NOT Country = 'Germany' AND NOT Country = 'USA';
```
