#  MySQL ALTER TABLE Statement

##  MySQL ALTER TABLE Statement

The `ALTER TABLE` statement is used to `add`, `delete`, or `modify`
columns in an existing table.

The `ALTER TABLE` statement is also used to add and drop
various constraints on an existing table.

##  ALTER TABLE - ADD Column

To add a column in a table, use the following syntax:

```sql
ALTER TABLE table_name
ADD column_name datatype;
```

> The following SQL adds an "Email" column to the "Customers" table:

```sql
ALTER TABLE Customers
    ADD Email varchar(255);
```

##  ALTER TABLE - DROP COLUMN

To delete a column in a table, use the following
syntax; notice that some database systems don't
allow deleting a column:

```sql
ALTER TABLE table_name
DROP COLUMN column_name;
```

> The following SQL deletes the "Email" column
> from the "Customers" table:

```sql
ALTER TABLE Customers
    DROP COLUMN Email;
```

ALTER TABLE - MODIFY COLUMN

To change the data type of a column in a table,
use the following syntax:

```sql
ALTER TABLE table_name
    MODIFY COLUMN column_name datatype;
```

##  MySQL ALTER TABLE Example

Look at the `Persons` table:

| ID |  LastName | FirstName |    Address   |    City   |
|:--:|:---------:|:---------:|:------------:|:---------:|
| 1  | Hansen    | Ola       | Timoteivn 10 | Sandnes   |
| 2  | Svendson  | Tove      | Borgvn 23    | Sandnes   |
| 3  | Pettersen | Kari      | Storgt 20    | Stavanger |

Now we want to add a column named `DateOfBirth` in the `Persons` table.

> We use the following SQL statement:

```sql
ALTER TABLE Persons
    ADD DateOfBirth date;
```

```text
Notice:
-------

The new column, `DateOfBirth`, is of type date and is going 
to hold a date. The data type specifies what type of data 
the column can hold. 

For a complete reference of all the data types available in 
MySQL, go to our complete Data Types reference.
```

The "Persons" table will now look like this:
| ID |  LastName | FirstName |    Address   |    City   | DateOfBirth |
|:--:|:---------:|:---------:|:------------:|:---------:|:-----------:|
| 1  | Hansen    | Ola       | Timoteivn 10 | Sandnes   |             |
| 2  | Svendson  | Tove      | Borgvn 23    | Sandnes   |             |
| 3  | Pettersen | Kari      | Storgt 20    | Stavanger |             |

##  Change Data Type Example

Now we want to change the data type of the column named
"DateOfBirth" in the "Persons" table.

> We use the following SQL statement:

```sql
ALTER TABLE Persons
    MODIFY COLUMN DateOfBirth year;
```

Notice that the "DateOfBirth" column is now of type year
and is going to hold a year in a two- or four-digit format.

##  DROP COLUMN Example

Next, we want to delete the column named "DateOfBirth" in the "Persons" table.

> We use the following SQL statement:

```sql
ALTER TABLE Persons
    DROP COLUMN DateOfBirth;
```

The "Persons" table will now look like this:
| ID |  LastName | FirstName |    Address   |    City   |
|:--:|:---------:|:---------:|:------------:|:---------:|
| 1  | Hansen    | Ola       | Timoteivn 10 | Sandnes   |
| 2  | Svendson  | Tove      | Borgvn 23    | Sandnes   |
| 3  | Pettersen | Kari      | Storgt 20    | Stavanger |
