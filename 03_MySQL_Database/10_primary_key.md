
# MySQL PRIMARY KEY Constraint

The `PRIMARY KEY` constraint uniquely identifies each
record in a table.

`Primary keys must contain UNIQUE values, and cannot contain NULL values.`

- A table can have `only ONE primary key`.
- this primary key can consist of `single or multiple columns` (fields).

## PRIMARY KEY on CREATE TABLE

> The following SQL creates a `PRIMARY KEY on the ID` column
> when the `Persons` table is created:

```sql
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    PRIMARY KEY (ID)
);
```

> To allow `naming of a PRIMARY KEY` constraint, and for `defining
a PRIMARY KEY constraint on multiple columns`, use the following
> SQL syntax:

```sql
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    CONSTRAINT PK_Person PRIMARY KEY (ID,LastName)
);
```

```text
Note: 
------

In the example above there is only ONE PRIMARY KEY (PK_Person). 
However, the VALUE of the primary key is made up of TWO COLUMNS
 (ID + LastName).
```

##  PRIMARY KEY on ALTER TABLE

> To create a PRIMARY KEY constraint on the "ID" column after
> the table had been already created, use the following SQL:

```sql
ALTER TABLE Persons
    ADD PRIMARY KEY (ID);
```

> To allow naming of a PRIMARY KEY constraint, and for
> defining a PRIMARY KEY constraint on multiple columns,
> use the following SQL syntax:

```sql
ALTER TABLE Persons
    ADD CONSTRAINT PK_Person PRIMARY KEY (ID,LastName);
```

```text
Note: 
------

If you use ALTER TABLE to add a primary key, the primary 
key column(s) must have been declared to not contain NULL 
values (when the table was first created).
```

## DROP a PRIMARY KEY Constraint

> To drop a PRIMARY KEY constraint, use the following SQL:

```sql
ALTER TABLE Persons
    DROP PRIMARY KEY;
```
