# :bulb: MySQL DATABASE

## :small_blue_diamond: MySQL CREATE DB

### The MySQL CREATE DATABASE Statement

The `CREATE DATABASE` statement is used to create a new SQL database.

**Syntax**

```sql
CREATE DATABASE databasename;
```

### CREATE DATABASE Example

The following SQL statement creates a database called "testDB":

**Example**

```sql
CREATE DATABASE testDB;
```

## :small_blue_diamond: MySQL DROP DB

### The MySQL DROP DATABASE Statement

The `DROP DATBASE` statement is used to drop an existing SQL database:

**Syntax**

```sql
DROP DATABASE databasename;
```

**Note**: Be careful before dropping a database. Deleting a database will result in loss of complete information stored in the database!

**Tip**: Make sure you have admin privilage before dropping any database. Once a database is dropped, you can check it in the list of databases with the following SQL command: `SHOW DATABASES;`

## :small_blue_diamond: MySQL CREATE TABLE

### The MySQL CREATE TABLE Statement

The `CREATE TABLE` statement is used to create a new table in a database.

**Syntax**

```sql
CREATE TABLE table_name (
  column1 datatype,
  column2 datatype,
  column3 datatype,
  ...
);
```

### MySQL CREATE TABLE Example

The following example creates a table called "Persons" that contains five columns: PersonID, LastName, FirtName, Address, and City:

**Example**

```sql
CREATE TABLE Persons (
  PersonID int,
  LastName varchar(255),
  FirstName varchar(255),
  Address varchar(255),
  City varchar(255)
);
```

**Tip**: The empty "Persons" table can now be filled with data with the SQL <u>INSERT INTO</u> statement.

### Create Table Using Another Table

A copy of an existing table can also be created using `CREATE TABLE`.

The new table gets the same column definition. All columns or specific columns can be selected.

If you create a new table using an exisiting table, the new table will be filled with the existing values from the old table.

**Syntax**

```sql
CREATE TABLE new_table_name AS
SELECT column1, column2, ...
FROM existing_table_name
WHERE ...;
```

The following SQL creates a new table called "TestTables" (which is a copy of the "Customers" table):

**Example**

```sql
CREATE TABLE TestTable AS
SELECT customerName, contactName
FROM Customers;
```

## :small_blue_diamond: MySQL DROP TABLE

### The MySQL DROP TABLE Statement

The `DROP TABLE` statement is used to drop an existing table in a database.

**Syntax**

```sql
DROP TABLE table_name;
```

**Note**: Be careful before dropping a table. Deleting a table will result in loss of complete information stored in the table!

### DROP TABLE Example

The following SQL statement drops an existing table "Shippers":

**Example**

```sql
DROP TABLE Shippers;
```

### TRUNCATE TABLE

The `TRUNCATE TABLE` statement is used to delete the data inside a table, but not the table itself

**Syntax**

```sql
TRUNCATE TABLE table_name;
```

## :small_blue_diamond: MySQL ALTER TABLE

### ALTER TABLE Statement

The `ALTER TABLE` statement is used to add, delete, or modify columns in an existing table.

The `ALTER TABLE` statement is also used to add and drop various constraints on an existing table.

### ALTER TABLE - ADD column

To add a column in a table, use the following syntax:

```sql
ALTER TABLE table_name ADD column_name datatype;
```

The following SQL adds an "Email" column to the "Customers" table:

```sql
ALTER TABLE Customers ADD Email varchar(255);
```

### ALTER TABLE - DROP column

To delete a column in a table,use the following syntax (notice that some database systems don't allow deleting a column)

```sql
ALTER TABLE table_name DROP COLUMN column_name;
```

The following SQL deletes the "Email" column from the "Customers" table:

```sql
ALTER TABLE Customers DROP COLUMN Email;
```

### ALTER TABLE - MODIFY COLUMN

To change the data type of a column in a table, use the following syntax:

```sql
ALTER TABLE table_name MODIFY COLUMN column_name datatype;
```

### ALTER TABLE Example

Now we want to add a column named "DateOfBirth" in the "Persons" table.

We use the following SQL statement:

**Example**

```sql
ALTER TABLE Persons ADD DateOfBirth date;
```

### Change Data Type Example

Now we want to change the data type of the column named "DateOfBirth" in the "Persons" table.

We use the following SQL statement:

**Example**

```sql
ALTER TABLE Persons MODIFY COLUMN DateOfBirth year;
```

### DROP COLUMN Example

Next, we want to delete the column named "DateOfBirth" in the "Persons" table.

We use the following SQL statement:

**Example**

```sql
ALTER TABLE Persons DROP COLUMN DateOfBirth;
```

## :small_blue_diamond: MySQL Constraints

### Create Constraints

Constraints can be specified when the table is created with the `CREATE TABLE` statement, or after the table is created with the `ALTER TABLE` statement.

**Syntax**

```sql
CREATE TABLE table_name (
  column1 datatype constraint,
  column2 datatype constraint,
  column3 datatype constraint,
  ...
);
```

### MySQL Constraints

SQL constraints are used to specify rules for the data in a table

Constraints are used to limit the type of data that can go into a table. This ensures the accuracy and reliability of the data in the table. If there is any violation between the constraint and the data action, the action is aborted.

Constraints can be a column level or table level. Column level constraints apply to a column, and table level constraints apply to the whole table.

The following constraints are commonly used in SQL:

- `NOT NULL` - Ensures that a column cannot have a NULL value
- `UNIQUE` - Ensures that all values in a column are different
- `PRIMARY KEY` - A combination of a `NOT NULL` and `UNIQUE`. Uniquely identifies each row in a table
- `FOREIGN KEY` - Prevents actions that would destroy links between tables
- `CHECK` - Ensures that the values in a column satisfies a special condition
- `DEFAULT` - Sets a default value for a column if no value is specified
- `CREATE INDEX` - Used to create and retrieve data from the database very quickly

## :small_blue_diamond: MySQL NOT NULL

### MySQL NOT NULL Constraint

By default, a column can hold NULL values.

The `NOT NULL` constraint enforces a column to NOT accept NULL values.

This enforces a field to always contain a value, which means that you cannot insert a new record, or update a record without adding a value to this field.

### NOT NULL on CREATE TABLE

The following SQL ensures that the "ID", "LastName", and "FirstName" columns will NOT accept NULL values when the "Persons" table is created:

**Example**

```sql
CREATE TABLE Persons (
  ID int NOT NULL,
  LastName varchar(255) NOT NULL,
  FirstName varchar(255) NOT NULL,
  Age int
);
```

### NOT NULL on ALTER TABLE

To create a `NOT NULL` constraint on the "Age" column when the "Persons" table is already created, use the following SQL:

**Example**

```sql
ALTER TABLE Persons MODIFY Age int NOT NULL;
```

## :small_blue_diamond: MySQL UNIQUE

### MySQL UNIQUE Constraint

The `UNIQUE` constraint ensures that all values in a column are different.

Both the `UNIQUE` and `PRIMARY KEY` constraints provide a guarantee for uniqueness for a column or set of columns.

A `PRIMARY KEY` constraint automatically has a `UNIQUE` constraint.

However, you can have many `UNIQUE` constraint per table, but only one `PRIMARY KEY` constraint per table.

### UNIQUE Constraint on CREATE TABLE

The following SQL creates a `UNIQUE` constraint on the "ID" column when the "Persons" table is created:

```sql
CREATE TABLE Persons (
  ID int NOT NULL,
  LastName varchar(255) NOT NULL,
  FirstName varchar(255),
  Age int,
  UNIQUE (ID)
);
```

To name a `UNIQUE` constraint, and to define a `UNIQUE` constraint on multiple columns, use the following SQL syntax:

```sql
CREATE TABLE Persons (
  ID int NOT NULL,
  LastName varchar(255) NOT NULL,
  FirstName varchar(255),
  Age int,
  CONSTRAINT UC_Person UNIQUE (ID, LastName)
);
```

### UNIQUE Constraint on ALTER TABLE

To create a `UNIQUE` constraint on the "ID" column when the table is already created, use the following SQL:

```sql
ALTER TABLE Persons ADD UNIQUE (ID);
```

To name a `UNIQUE` constraint, and to define a `UNIQUE` constraint on multiple columns, use the following SQL syntax:

```sql
ALTER TABLE Persons ADD CONSTRAINT UC_Person UNIQUE (ID, LastName);
```

### DROP a UNIQUE Constraint

To drop a `UNIQUE` constraint, use the following SQL:

```sql
ALTER TABLE Persons DROP INDEX UC_Person;
```

## :small_blue_diamond: MySQL PRIMARY KEY

### MySQL PRIMARY KEY Constraint

The `PRIMARY KEY` constraint uniquely identifies each record in a table. 

Primary keys must contain UNIQUE value, and cannot contain NULL values.

A table can have only ONE primary key; and in the table, this primary key can consist of single or multiple columns (fields).

### PRIMARY KEY on CREATE TABLE

The following SQL creates a `PRIMARY KEY` on the "ID" column when the "Persons" table is created:

```sql
CREATE TABLE Persons (
  ID int NOT NULL,
  LastName varchar(255) NOT NULL,
  FirstName varchar(255),
  Age int,
  PRIMARY KEY (ID)
);
```

To allow naming of a `PRIMARY KEY` constraint, and for defining a `PRIMARY KEY` constraint on multiple columns, use the following SQL syntax:

```sql
CREATE TABLE Persons (
  ID int NOT NULL,
  LastName varchar(255) NOT NULL,
  FirstName varchar(255),
  Age int,
  CONSTRAINT PK_Person PRIMARY KEY (ID, LastName)
);
```

**NOTE**: In the example above there is only ONE `PRIMARY KEY` (PK_Person). However, the VALUE of the primary key is made up of TWO COLUMNS (ID + LastName).

### PRIMARY KEY on ALTER TABLE

To create a `PRIMARY KEY` constraint on the "ID" column when the table is already created, use the following SQL:

```sql
ALTER TABLE Persons ADD PRIMARY KEY (ID);
```

To allow naming of a `PRIMARY KEY` constraint, and for defining a `PRIMARY KEY` constraint on multiple columns, use the following SQL syntax:

```sql
ALTER TABLE Persons ADD CONSTRAINT PK_Person PRIMARY KEY (ID, LastName);
```

**NOTE**: If you use `ALTER TABLE` to add a primary key, the primary key column(s) must have been declared to not contain NULL values (when the table was first created).

### DROP a PRIMARY KEY Constraint

To drop a `PRIMARY KEY` constraint, use the following SQL:

```sql
ALTER TABLE Persons DROP PRIMARY KEY;
```

## :small_blue_diamond: MySQL FOREIGN KEY

### MySQL FOREIGN KEY Constraint

The `FOREIGN KEY` constraint is used to prevent actions that would destroy links between tables.

A `FOREIGN KEY` is a field (or collections of fields) in one table, that refers to the `PRIMARY KEY` in another table.

The table with the foreign key is called the child table, and the table with the primary key is called the referenced or parent table.

### FOREIGN KEY on CREATE TABLE

The following SQL creates a `FOREIGN KEY` on the "PersonID" column when the "Orders" tables is created:

```sql
CREATE TABLE Orders (
  OrderID int NOT NULL,
  OrderNumber int NOT NULL,
  PersonID int,
  PRIMARY KEY (OrderID),
  FOREIGN KEY (PersonID) REFERENCES Persons(PersonID)
);
```

To allow naming of a `FOREIGN KEY` constraint, and for defining a `FOREIGN KEY` constraint on multiple columns, use the following syntax:

```sql
CREATE TABLE Orders (
  OrderID int NOT NULL,
  OrderNumber int NOT NULL,
  PersonID int,
  PRIMARY KEY (OrderID),
  CONSTRAINT FK_PersonOrder FOREIGN KEY (PersonID) REFERENCES Person(PersonID)
);
```

### FOREIGN KEY on ALTER TABLE

To create a `FOREIGN KEY` constraint on the "PersonID" column when the "Orders" table is already created, use the following SQL:

```sql
ALTER TABLE Orders ADD FOREIGN KEY (PersonID) REFERENCES Persons(PersonID);
```

To allow naming of a `FOREIGN KEY` constraint, and for defining a `FOREIGN KEY` constraint on multiple columns, use the following syntax:

```sql
ALTER TABLE ADD CONSTRAINT FK_PersonOrder FOREIGN KEY (PersonID) REFERENCES Persons(PersonID);
```

### DROP a FOREIGN KEY Constraint

To drop a `FOREIGN KEY` constraint, use the following SQL:

```sql
ALTER TABLE Orders DROP FOREIGN KEY FK_PersonOrder;
```

## :small_blue_diamond: MySQL CHECK

### MySQL CHECK Constraint

The `CHECK` constraint is used to limit the value range that can be placed in a column.

If you define a `CHECK` constraint on a column it will allow only certain values for this column.

If you define a `CHECK` constraint on a table it can limit the values in certain columns based on values in other columns in the row.

### CHECK on CREATE TABLE

The following SQL creates a `CHECK` constraint on the "Age" column when the "Persons" table is created. The `CHECK` constraint ensures that the age of a person must be 18, or older:

```sql
CREATE TABLE Persons (
  ID int NOT NULL,
  LastName varchar(255) NOT NULL,
  FirstName varchar(255),
  Age int,
  CHECK (Age >= 18)
);
```

To allow naming of a `CHECK` constraint and for defining a `CHECK` constraint on multiple columns, use the following SQL syntax:

```sql
CREATE TABLE Persons (
  ID int NOT NULL,
  LastName varchar(255) NOT NULL,
  FirstName varchar(255),
  Age int,
  City varchar(255),
  CONSTRAINT CHK_Person CHECK (Age >= 18 AND City='Sandnes')
);
```

### CHECK on ALTER TABLE

To create a `CHECK` constraint on the "Age" column when the table is already created, use the following SQL:

```sql
ALTER TABLE Persons ADD CHECK (Age >= 18);
```

To allow naming of a `CHECK` constraint, and for defining a `CHECK` constraint on multiple columns, use the following SQL syntax:

```sql
ALTER TABLE Persons ADD CONSTRAINT CHK_PersonAge CHECK (Age >= 18 AND City='Sandnes');
```

### DROP a CHECK Constraint

To drop a `CHECK` constraint, use the following SQL:

```sql
ALTER TABLE Persons DROP CHECK CHK_PersonAge;
```
