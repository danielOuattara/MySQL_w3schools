# MySQL UNIQUE Constraint

The `UNIQUE` constraint ensures that all the values in
a column are different.

Both the `UNIQUE` and `PRIMARY KEY` constraints provide
a guarantee for `uniqueness` for a column or set of columns.

A `PRIMARY KEY` constraint automatically has a UNIQUE constraint.

However, you can have `many UNIQUE` constraints per table,
but `only one PRIMARY KEY` constraint per table.

##  UNIQUE Constraint on CREATE TABLE

> The following SQL creates a `UNIQUE` constraint on the `ID`
> column when the `Persons` table is created:

```sql
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    UNIQUE (ID)
);
```

> `To name and to define a UNIQUE constraint` on
> multiple columns, use the following SQL syntax:

```sql
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    CONSTRAINT UC_Person UNIQUE (ID,LastName)
);
```

##  UNIQUE Constraint on ALTER TABLE

> `To create a UNIQUE constraint` on the `ID` column when the table
> is already created, use the following SQL:

```sql
ALTER TABLE Persons
    ADD UNIQUE (ID);
```

> `To name and to define a UNIQUE constraint` on
> multiple columns, use the following SQL syntax:

```sql
ALTER TABLE Persons
    ADD CONSTRAINT UC_Person UNIQUE (ID,LastName);
```

##  DROP a UNIQUE Constraint

> `To drop a UNIQUE constraint`, use the following SQL:

```sql
ALTER TABLE Persons
    DROP INDEX UC_Person;
```
