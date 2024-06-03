# MySQL RDBMS

## What is RDBMS?

`RDBMS` stands for Relational Database Management System.

`RDBMS` is a program used to maintain a relational database.

`RDBMS` is the basis for all modern database systems such as
MySQL, Microsoft SQL Server, Oracle, and Microsoft Access.

`RDBMS` uses SQL queries to access the data in the database.

## What is a Database Table?

A table is a collection of related data entries, and it
consists of columns and rows.

- A column holds specific information about every record in the table.

- A record (or row) is each individual entry that exists in a table.

### Look at a selection from the Northwind "Customers" table

| CustomerID |            CustomerName            |     ContactName    |            Address            |     City    | PostalCode | Country |
|:----------:|:----------------------------------:|:------------------:|:-----------------------------:|:-----------:|:----------:|:-------:|
| 1          | Alfreds Futterkiste                | Maria Anders       | Obere Str. 57                 | Berlin      | 12209      | Germany |
| 2          | Ana Trujillo Emparedados y helados | Ana Trujillo       | Avda. de la Constitución 2222 | México D.F. | 05021      | Mexico  |
| 3          | Antonio Moreno Taquería            | Antonio Moreno     | Mataderos 2312                | México D.F. | 05023      | Mexico  |
| 4          | Around the Horn                    | Thomas Hardy       | 120 Hanover Sq.               | London      | WA1 1DP    | UK      |
| 5          | Berglunds snabbköp                 | Christina Berglund | Berguvsvägen 8                | Luleå       | S-958 22   | Sweden  |

The columns in the **`Customers`** table above are:

- `CustomerID`
- `CustomerName`
- `ContactName`
- `Address`,
- `City`,
- `PostalCode`
- `Country`.
  
The table has 5 records (rows).

## What is a Relational Database?

A relational database defines database relationships in the form of
tables. The tables are related to each other - based on data common
to each.

Look at the following three tables `Customers`, `Orders`, and
`Shippers` from the Northwind database:

###  Customers Table

| CustomerID |            CustomerName            |     ContactName    |            Address            |     City    | PostalCode | Country |
|:----------:|:----------------------------------:|:------------------:|:-----------------------------:|:-----------:|:----------:|:-------:|
| 1          | Alfreds Futterkiste                | Maria Anders       | Obere Str. 57                 | Berlin      | 12209      | Germany |
| 2          | Ana Trujillo Emparedados y helados | Ana Trujillo       | Avda. de la Constitución 2222 | México D.F. | 05021      | Mexico  |
| 3          | Antonio Moreno Taquería            | Antonio Moreno     | Mataderos 2312                | México D.F. | 05023      | Mexico  |
| 4          | Around the Horn                    | Thomas Hardy       | 120 Hanover Sq.               | London      | WA1 1DP    | UK      |
| 5          | Berglunds snabbköp                 | Christina Berglund | Berguvsvägen 8                | Luleå       | S-958 22   | Sweden  |

The relationship between the `Customers` table and the `Orders` table
is the `CustomerID` column:

### Orders Table

| OrderID | CustomerID | EmployeeID |  OrderDate | ShipperID |
|:-------:|:----------:|:----------:|:----------:|:---------:|
| 10278   | 5          | 8          | 1996-08-12 | 2         |
| 10280   | 5          | 2          | 1996-08-14 | 1         |
| 10308   | 2          | 7          | 1996-09-18 | 3         |
| 10355   | 4          | 6          | 1996-11-15 | 1         |
| 10365   | 3          | 3          | 1996-11-27 | 2         |
| 10383   | 4          | 8          | 1996-12-16 | 3         |
| 10384   | 5          | 3          | 1996-12-16 | 3         |

The relationship between the `Orders` table and the `Shippers` table
is the `ShipperID` column:

### Shippers Table

| ShipperID |    ShipperName   |      Phone     |
|:---------:|:----------------:|:--------------:|
| 1         | Speedy Express   | (503) 555-9831 |
| 2         | United Package   | (503) 555-3199 |
| 3         | Federal Shipping | (503) 555-9931 |
