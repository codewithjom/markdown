# :point_right: Learn Basic SQL

> (c) 2022 w3schools/sql. Use of this is for a user to help whenever not online.

## Table of Contents

- [Introduction](#org2197275)
    - [What is SQL?](#org07eedcf)
    - [What Can SQL do?](#orgcebe03d)
    - [SQL is a Standard - BUT&#x2026;](#org18a1818)
    - [Using SQL in Your Web Site](#org43d6fb0)
    - [RDBMS](#orgaec71d0)
- [Syntax](#org93f7e3c)
    - [Database Tables](#orgdfcc65f)
    - [SQL Statements](#org36e3422)
    - [Keep in Mind That&#x2026;](#orgd67e13b)
    - [Semicolon after SQL Statements?](#orgbe81ffd)
    - [Some of The Most Important SQL Commands](#orgaa71e36)
- [SELECT Statement](#orgc67e44f)
    - [The SQL SELECT Statement](#orgd733b5e)
    - [Demo Database](#org748d507)
    - [SELECT Column Example](#org7d17d49)
    - [SELECT \* Example](#orgd0a60b9)
- [SELECT DISTINCT](#org9edbe75)
    - [The SQL SELECT DISTINCT Statement](#org5738f57)
    - [Demo Database](#org53ee854)
    - [SELECT Example Without DISTINCT](#org8d98c08)
    - [SELECT DISTINCT Examples](#org59a481f)
- [WHERE](#org7da8d32)
    - [The SQL WHERE Clause](#orgd82e7f4)
    - [Demo Database](#orgbd4d0c3)
    - [WHERE Clause Example](#org6affa75)
    - [Text Fields vs Numeric Fields](#orgdae6321)
    - [Operators in The WHERE Clause](#orgf066025)
- [AND, OR, NOT](#orgb0c3e04)
    - [The SQL AND, OR, and NOT Operators](#orgc4277bd)
    - [Demo Database](#org811de0f)
    - [AND Example](#orgdb63ea6)
    - [OR Example](#orgbb64cd8)
    - [NOT Example](#orgf42131d)
    - [Combining AND, OR and NOT](#orgc2aa745)
- [ORDER BY](#org0a15636)
    - [The SQL ORDER BY Keyword](#orge4bb452)
    - [Demo Database](#orgc8c9d2a)
    - [ORDER BY Example](#orgdb5bc43)
    - [ORDER BY DESC Example](#org75f7cea)
    - [ORDER BY Several Columns Example](#orgd6d4e8e)
    - [ORDER BY Several Columns Example 2](#org5cd536b)
- [INSERT INTO](#orgfdcc923)
    - [The SQL INSERT INTO Statement](#org70bf654)
    - [Demo Database](#org29f86b9)
    - [INSERT INTO Example](#org3c49f36)
    - [Insert Data Only in Specified Columns](#org132841d)
- [NULL Values](#org19c6247)
    - [What is NULL Value?](#orgb9d0260)
    - [How to Test for NULL Values?](#org74b964b)
    - [Demo Database](#org446b787)
    - [The IS NULL Operator](#org997e8f2)
    - [The IS NOT NULL Operator](#org3cf63cb)
- [UPDATE](#orgb4b7d4b)
    - [The SQL UPDATE Statement](#orge393a3e)
    - [Demo Database](#org36ecb8e)
    - [UPDATE Table](#orgdea5c01)
    - [UPDATE Multiple Records](#org9dbd0f0)
    - [Update WARNING!](#org74ed77b)
- [DELETE](#orga029582)
    - [The SQL DELETE Statement](#orga9455cc)
    - [Demo Database](#org02b14f7)
    - [SQL DELETE Example](#orgdaafb3f)
    - [Delete All Records](#org4412b2e)
- [SELECT TOP](#org73887db)
    - [The SQL SELECT TOP Clause](#org66f038e)
    - [Demo Database](#orgb6abce3)
    - [SQL, TOP, LIMIT, and FETCH FIRST Examples](#orgccd8f64)
    - [SQL TOP PERCENT Example](#org04c2558)
    - [ADD a WHERE CLAUSE](#orga2b2c36)
- [MIN and MAX](#org27dc513)
    - [The SQL MIN() and MAX() Functions](#org96fbfec)
    - [Demo Database](#orge006f89)
    - [MIN() Example](#orged4e082)
    - [MAX() Example](#org273cf00)
- [COUNT, AVG, SUM](#orgfa0dc0f)
    - [The SQL COUNT(), AVG(), and SUM() Functions](#orgbf3562c)
    - [Demo Database](#orgd9a2194)
    - [COUNT() Example](#orgdf7e29e)
    - [AVG() Example](#org4571eba)
    - [Demo Database](#org26d6180)
    - [SUM() Example](#org436917f)
- [LIKE](#orgba1eeeb)
    - [The SQL LIKE Operator](#org6e80b8d)
    - [Demo Database](#orgfcd4c14)
    - [SQL LIKE Examples](#org021a981)
- [Wildcards](#org299a469)
    - [SQL Wildcard Characters](#orgd127ce7)
    - [Demo Database](#orgaf9f6b8)
    - [Using the % Wildcard](#org659c183)
    - [Using the \_ Wildcard](#org7759167)
    - [Using the [charlist] Wildcard](#org5143e9c)
    - [Using the [!charlist] Wildcard](#org3c677ad)
- [IN](#org331a045)
    - [The SQL IN Operator](#org7e307a4)
    - [Demo Database](#org3912710)
    - [IN Operator Examples](#orgbf2b762)
- [BETWEEN](#org9ea4fcd)
    - [The SQL BETWEEN Operator](#org4f75bae)
    - [Demo Database](#orgc35dae0)
    - [BETWEEN Example](#orgec8bb3a)
    - [NOT BETWEEN Example](#orgeb25e60)
    - [BETWEEN with IN Example](#org319087e)
    - [BETWEEN Text Values Example](#org1b8c652)
    - [NOT BETWEEN Text Values Example](#org6dd98ec)
    - [Sample Table](#org319b1a2)
    - [BETWEEN Dates Example](#org27c8445)


<a id="org2197275"></a>

# Introduction

SQL is a standard language for accessing and manipulating databases.

<a id="org07eedcf"></a>

## What is SQL?

- SQL stands for Structured Query Language
- SQL lets you access and manipulate database
- SQL became a standard of the American National Standards Institue (ANSI) in 1986, and of the International Organization for Standardization (ISO) in 1987

<a id="orgcebe03d"></a>

## What Can SQL do?

- SQL can execute queries against a database
- SQL can retrieve data from a database
- SQL can insert records in a database
- SQL can update records in a database
- SQL can delete records from a database
- SQL can create new databases
- SQL can create new tables in a database
- SQL can create stored procedures in a database
- SQL can create vies in a database
- SQL can set permissions on tables, procedures, and views

<a id="org18a1818"></a>

## SQL is a Standard - BUT&#x2026;

Although SQL is an ANSI/ISO standard, there are different versions of the SQL language.

However, to be complaint with the ANSI standard, they all support at least the major commands (such as `SELECT`, `UPDATE`, `DELETE`, `INSERT`, `WHERE`) in a similar manner.

> :book: **Note**: Most of the SQL database programs also have their own proprietary extensions in addition to the SQL standard!

<a id="org43d6fb0"></a>

## Using SQL in Your Web Site

To build a web site that shows data from a database, you will need:

- RDBMS database program (i.e. MS Access, SQL Server, MySQL)
- To use a server-side scripting language, like PHP or ASP
- To use SQL to get the data you want
- To use HTML/CSS to style the page

<a id="orgaec71d0"></a>

## RDBMS

RDBMS stands for Relational Database Management System.

RDBMS is the basis for SQL, and for all modern database systems such as MS SQL Server, IBM DB2, Oracle, MySQL, and Microsoft Access.

The data in RDBMS is stored in database objects called tables. A table is a collection of related data entries and it consists of columns and rows.

Look at the "Customers" table:

**Example**

``` sql
SELECT * FROM Customers;
```

Every table is broken up into smaller entities called fields. The fields in the Customers table consist of CustomerID, CustomerName, ContactName, Address, City, PostalCode and Country. A field is a column in a table that is designed to maintain specific information about every record in the table.

A record, also called a row, is each individual entry that exists in a table. For example, there are 91 records in the above Customers table. A record is a horizontal entity in a table.

A column is a vertical entity in a table that contains all information associated with a specific field in a table.

<a id="org93f7e3c"></a>

# Syntax

<a id="orgdfcc65f"></a>

## Database Tables

A database most often contains one or more tables. Each table is identified by a name (e.g. "Customers" or "Orders"). Tables contain records (rows) with data.

In this tutorial we will use the well-known Northwind sample database (included in MS Access and MS SQL Server).

Below is a selection from the "Customers" table:

![img](/img/db-table.png)

The table above contains five records (one for each customer) and seven columns (CustomerID, CustomerName, ContactName, Address, City, PostalCode, and Country).

<a id="org36e3422"></a>

## SQL Statements

Most of the actions you need to perform on a database are done with SQL statements.

The following SQL statement selects all the records in the "Customers" table:

**Example**

``` sql
SELECT * FROM Customers;
```

In this tutorial we will teach you all about the different SQL statements.

<a id="orgd67e13b"></a>

## Keep in Mind That&#x2026;

- SQL keywords are NOT case sensitive: `select` is the same as `SELECT`

In this tutorial we will write all SQL keywords in upper-case.

<a id="orgbe81ffd"></a>

## Semicolon after SQL Statements?

Some database systems requires a semicolon at the end of each SQL statement.

Semicolon is the standard way to separate each SQL statement in database systems that allow more than one SQL statement to be executed in the same call to the server.

In this tutorial, we will use semicolon at the end of each SQL statement.

<a id="orgaa71e36"></a>

## Some of The Most Important SQL Commands

- `SELECT` - extracts data from a database
- `UPDATE` - updates data in a database
- `DELETE` - deletes data from a database
- `INSERT INTO` - inserts new data into a database
- `CREATE DATABASE` - creates a new database
- `ALTER DATABASE` - modifies a database
- `CREATE TABLE` - creates a new table
- `ALTER TABLE` - modifies a table
- `DROP TABLE` - deletes a table
- `CREATE INDEX` - creates an index (search key)
- `DROP INDEX` - deletes an index

<a id="orgc67e44f"></a>

# SELECT Statement

<a id="orgd733b5e"></a>

## The SQL SELECT Statement

The `SELECT` statement is used to select data from a database.

The data returned is stored in a result table, called the result-set.

**SELECT Syntax**

``` sql
SELECT column1, column2, ...
FROM table_name;
```

Here, column1, column2, &#x2026; are the field names of the table you want to select data from. If you want to select all the fields available in the table, use the following syntax:

``` sql
SELECT * FROM table_name;
```

<a id="org748d507"></a>

## Demo Database

Below is a selection from the "Customers" table in the Northwind sample database:

![img](/img/db-table.png)

<a id="org7d17d49"></a>

## SELECT Column Example

The following SQL statement selects the "CustomerName" and "City" columns from the "Customers" table:

**Example**

``` sql
SELECT CustomerName, City FROM Customers;
```

<a id="orgd0a60b9"></a>

## SELECT \* Example

The following SQL statement selects all the columns from the "Customers" table:

**Example**

``` sql
SELECT * FROM Customers;
```

<a id="org9edbe75"></a>

# SELECT DISTINCT

<a id="org5738f57"></a>

## The SQL SELECT DISTINCT Statement

The `SELECT DISTINCT` statement is used to return only distinct (different) values.

Inside a table, a column often contains many duplicate values; and sometimes you only want to list the different (distinct) values.

**SELECT DISTINCT Syntax**

``` sql
SELECT DISTINCT column1, column2, ...
FROM table_name;
```

<a id="org53ee854"></a>

## Demo Database

Below is a selection from the "Customers" table in the Northwind sample database:

![img](/img/db-table.png)

<a id="org8d98c08"></a>

## SELECT Example Without DISTINCT

The following SQL statement selects all (including the duplicates) values from the "Country" column in the "Customers" table:

**Example**

``` sql
SELECT Country FROM Customers;
```

Now, let us use the `SELECT DISTINCT` statement and see the result.

<a id="org59a481f"></a>

## SELECT DISTINCT Examples

The following SQL statement selects only the DISTINCT values from the "Country" column in the "Customers" table:

**Example**

``` sql
SELECT DISTINCT Country FROM Customers;
```

The following SQL statement lists the number of different (distinct) customer countries:

**Example**

``` sql
SELECT COUNT(DISTINCT Country) FROM Customers;
```

> :book: **Note**: **The example above will not work in Firefox!** Because COUNT(DISTINCT *columnname*) is not supported in Microsoft Access database. Firefox is using Microsoft Access in our examples.

Here is the workaround for MS Access:

**Example**

``` sql
SELECT Count(*) AS DistinctCountries
FROM (SELECT DISTINCT Country FROM Customers);
```

<a id="org7da8d32"></a>

# WHERE

<a id="orgd82e7f4"></a>

## The SQL WHERE Clause

The `WHERE` clause is used to filter records.

It is used to extract only those records that fulfill a specified condition.

**WHERE Syntax**

``` sql
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```

> :book: **Note**: The `WHERE` clause is not only used in `SELECT` statements, it is also used in `UPDATE`, `DELETE`, etc.!

<a id="orgbd4d0c3"></a>

## Demo Database

Below is a selection from the "Customers" table in the Northwind sample database:

![img](/img/db-table.png)

<a id="org6affa75"></a>

## WHERE Clause Example

The following SQL statement selects all the customers from the country "Mexico", in the "Customers" table:

**Example**

``` sql
SELECT * FROM Customers WHERE Country='Mexico';
```

<a id="orgdae6321"></a>

## Text Fields vs Numeric Fields

SQL requires single quotes around text values (most database systems will also allow double quotes).

However, numeric fields should not be enclosed in quotes:

**Example**

``` sql
SELECT * FROM Customers WHERE CustomerID=1;
```

<a id="orgf066025"></a>

## Operators in The WHERE Clause

The following operators can be used in the `WHERE` clause:

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">

<colgroup>
<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left"><b>Operator</b></th>
<th scope="col" class="org-left"><b>Description</b></th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">=</td>
<td class="org-left">Equal</td>
</tr>


<tr>
<td class="org-left">&gt;</td>
<td class="org-left">Greater than</td>
</tr>


<tr>
<td class="org-left">&lt;</td>
<td class="org-left">Less than</td>
</tr>


<tr>
<td class="org-left">&gt;=</td>
<td class="org-left">Greater than or equal to</td>
</tr>


<tr>
<td class="org-left">&lt;=</td>
<td class="org-left">Less than or equal to</td>
</tr>


<tr>
<td class="org-left">&lt;&gt;</td>
<td class="org-left">Not equal. <b>Note</b>: In some versions of SQL this operator may be written as !=</td>
</tr>


<tr>
<td class="org-left">BETWEEN</td>
<td class="org-left">Between a certain range</td>
</tr>


<tr>
<td class="org-left">LIKE</td>
<td class="org-left">Search for a pattern</td>
</tr>


<tr>
<td class="org-left">IN</td>
<td class="org-left">To specify multiple possible values fro a column</td>
</tr>
</tbody>
</table>

<a id="orgb0c3e04"></a>

# AND, OR, NOT

<a id="orgc4277bd"></a>

## The SQL AND, OR, and NOT Operators

The `WHERE` clause can be combined with `AND`, `OR`, and `NOT` operators.

The `AND` and `OR` operators are used to filter records based on more than one condition:

- The `AND` operator displays a records if all the conditions separated by `AND` are TRUE.
- The `OR` operator displays a record if any of the conditions separated by `OR` is TRUE.

The `NOT` operator displays a records if the condition(s) is NOT TRUE.

**AND Syntax**

``` sql
SELECT column1, column2, ...
FROM table_name
WHERE condition1 AND condition2 AND condition3 ...;
```

**OR Syntax**

``` sql
SELECT column1, column2, ...
FROM table_name
WHERE condition1 OR condition2 OR condition3 ...;
```

**NOT Syntax**

``` sql
SELECT column1, column2, ...
FROM table_name
WHERE NOT condition;
```

<a id="org811de0f"></a>

## Demo Database

The table below shows the complete "Customers" table from the Northwind sample database:

![img](/img/db-table2.png)

<a id="orgdb63ea6"></a>

## AND Example

The following SQL statement selects all fields from "Customers" where country is "Germany" AND city is "Berlin":

**Example**

``` sql
SELECT * FROM Customers WHERE Country='Germany' AND City='Berlin';
```

<a id="orgbb64cd8"></a>

## OR Example

The following SQL statement selects all fields from "Customers" where city is "Berlin" or "München":

**Example**

``` sql
SELECT * FROM Customers WHERE City='Berlin' OR City='München';
```

The following SQL statement selects all fields from "Customers" where country is "Germany" OR "Spain":

**Example**

``` sql
SELECT * FROM Customers
WHERE Country='Germany' OR Country='Spain';
```

<a id="orgf42131d"></a>

## NOT Example

The following SQL statement selects all fields from "Customers" where country is NOT "Germany":

**Example**

``` sql
SELECT * FROM Customers
WHERE NOT Country='Germany';
```

<a id="orgc2aa745"></a>

## Combining AND, OR and NOT

You can also combine the `AND`, `OR` and `NOT` operators.

The following SQL statement selects all fields from "Customers" where country is "Germany" AND city must be "Berlin" OR "München" (use parenthesis to form complex expressions):

**Example**

``` sql
SELECT * FROM Customers
WHERE Country='Germany' AND (City='Berlin' OR City='München')
```

The following SQL statement selects all fields from "Customers" where country is NOT "Germany" and NOT "USA":

**Example**

``` sql
SELECT * FROM Customers
WHERE NOT Country='Germany' AND NOT Country='USA';
```

<a id="org0a15636"></a>

# ORDER BY

<a id="orge4bb452"></a>

## The SQL ORDER BY Keyword

The `ORDER BY` keyword is used to sort the result-set in ascending or descending order.

The `ORDER BY` keyword sorts the records in ascending order by default. To sort the records in descending order, use the `DESC` keyword.

**ORDER BY Syntax**

``` sql
SELECT column1, column2, ...
FROM table_name
ORDER BY column1, column2, ... ASC|DESC;
```

<a id="orgc8c9d2a"></a>

## Demo Database

Below is a selection from the "Customers" table in the Northwind sample database:

![img](/img/db-table.png)

<a id="orgdb5bc43"></a>

## ORDER BY Example

The following SQL statement selects all customers from the "Customers" table, sorted by the "Country" column:

**Example**

``` sql
SELECT * FROM Customers ORDER BY Country;
```

<a id="org75f7cea"></a>

## ORDER BY DESC Example

The following SQL statement selects all customers from the "Customers" table, sorted DESCENDING by the "Country" column:

**Example**

``` sql
SELECT * FROM Customers ORDER BY Country DESC
```

<a id="orgd6d4e8e"></a>

## ORDER BY Several Columns Example

The following SQL statement selects all customers from the "Customers" table, sorted by the "Country" and the "CustomerName" column. This means that it orders by Country, but if some rows have the same Country, it orders them by CustomerName:

**Example**

``` sql
SELECT * FROM Customers ORDER BY Country, CustomerName;
```

<a id="org5cd536b"></a>

## ORDER BY Several Columns Example 2

The following SQL statement selects all customers from the "Customers" table, sorted ascending by the "Country" and descending by the "CustomerName" column:

**Example**

``` sql
SELECT * FROM Customers ORDER BY Country ASC, CustomerNAme DESC;
```

<a id="orgfdcc923"></a>

# INSERT INTO

<a id="org70bf654"></a>

## The SQL INSERT INTO Statement

The `INSERT INTO` statement is used to insert new records in a table.

**INSERT TO Syntax**

It is possible to write the `INSERT INTO` statement in two ways:

1. Specify both the column names and the values to be inserted:

``` sql
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);
```

2. If you are adding values for all the columns of the table, you do not need to specify the column names in the SQL query. However, make sure the order of the values is in the same order as the columns in the table. Here, the `INSERT INTO` syntax would be as follows:

``` sql
INSERT INTO table_name
VALUES (value1, value2, value3, ...);
```

<a id="org29f86b9"></a>

## Demo Database

Below is a selection from the "Customers" table in the Northwind sample database:

![img](/img/db-table3.png)

<a id="org3c49f36"></a>

## INSERT INTO Example

The following SQL statement inserts a new record in the "Customers" table:

**Example**

``` sql
INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country)
VALUES ('Cardinal', 'Tom B. Erichsen', 'Skagen 21', 'Stavanger', '4006', 'Norway');
```

The selection from the "Customers" table will now look like this:

![img](/img/db-table4.png)

> :bulb: **Did you notice that we did not insert any number into the CustomerID field?**

The CustomerID column is an <u>auto-increment</u> field and will be generated automatically when a new record is inserted into the table.

<a id="org132841d"></a>

## Insert Data Only in Specified Columns

It is also possible to only insert data in specific columns.

The following SQL statement will insert a new record, but only insert data in the "CustomerName", "City", and "Country" columns (CustomerID will be updated automatically);

**Example**

``` sql
INSERT INTO Customers (CustomerName, City, Country)
VALUES ('Cardinal', 'Stavanger', 'Norway');
```

The selection from the "Customers" table will now look like this:

![img](/img/db-table5.png)

<a id="org19c6247"></a>

# NULL Values

<a id="orgb9d0260"></a>

## What is NULL Value?

A field with a NULL value is a field with no value.

If a field in a table is optional, it is possible to insert a new record or update a record without adding a value to this field. Then, the field will be saved with a NULL value.

> :book: **Note**: A NULL value is different from a zero value or a field that contains spaces. A field with a NULL value is one that has been left blank during record creation!

<a id="org74b964b"></a>

## How to Test for NULL Values?

It is not possible to test for NULL values with comparison operators, such as =, <, or <>.

We will have to use the `IS NULL` and `IS NOT NULL` operators instead.

**IS NULL Syntax**

``` sql
SELECT column_names FROM table_name WHERE column_name IS NULL;
```

**IS NOT NULL Syntax**

``` sql
SELECT column_names FROM table_name WHERE column_name IS NOT NULL;
```

<a id="org446b787"></a>

## Demo Database

Below is a selection from the "Customers" table in the Northwind sample database:

![img](/img/db-table.png)

<a id="org997e8f2"></a>

## The IS NULL Operator

The `IS NULL` operator is used to test for empty values (NULL values).

The following SQL lists all customers with a NULL value in the "Address" field:

**Example**

``` sql
SELECT CustomerName, ContactName, Address FROM Customers WHERE Address IS NULL;
```

> :bulb: **Tip**: Always use IS NULL to look for NULL values.

<a id="org3cf63cb"></a>

## The IS NOT NULL Operator

The `IS NOT NULL` operator is used to test for non-empty values (NOT NULL values).

The following SQL lists all customers with a value in the "Address" field:

**Example**

``` sql
SELECT CustomerName, ContactName, Address FROM Customers WHERE Address IS NOT NULL;
```

<a id="orgb4b7d4b"></a>

# UPDATE

<a id="orge393a3e"></a>

## The SQL UPDATE Statement

The `UPDATE` statement is used to modify the existing records in a table.

**UPDATE Syntax**

``` sql
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```

> :book: **Note**: Be careful when updating records in a table! Notice the `WHERE` clause in the `UPDATE` statement. The `WHERE` clause specifies which record(s) that should be updated.

<a id="org36ecb8e"></a>

## Demo Database

Below is a selection from the "Customers" table in the Northwind sample database:

![img](/img/db-table.png)

<a id="orgdea5c01"></a>

## UPDATE Table

The following SQL statement updates the first customer (CustomerID = 1) with a new contact person *and* a new city.

**Example**

``` sql
UPDATE Customers SET ContactName = 'Alfred Schmidt', City = 'Frankfurt' WHERE CustomerID = 1;
```

The selection from the "Customers" table will now look like this:

![img](/img/db-table6.png)

<a id="org9dbd0f0"></a>

## UPDATE Multiple Records

It is the `WHERE` clause that determines how many records will be updated.

The following SQL statement will update the ContactName to "Juan" for all records where country is "Mexico":

**Example**

``` sql
UPDATE Customers SET ContactName='Juan' WHERE Country='Mexico';
```

The selection from the "Customers" table will now look like this:

![img](/img/db-table7.png)

<a id="org74ed77b"></a>

## Update WARNING!

Be careful when updating records. If you omit the `WHERE` clause, ALL records will be updated!

**Example**

``` sql
UPDATE Customers SET ContactName='Juan';
```

The "Customers" table will change all the ContactName to Juan.

<a id="orga029582"></a>

# DELETE

<a id="orga9455cc"></a>

## The SQL DELETE Statement

The `DELETE` statement is used to delete exisiting records in a table.

**DELETE Syntax**

``` sql
DELETE FROM table_name WHERE condition;
```

> :book: **Note**: Be careful when deleting records in a table! Notice the `WHERE` clause in the `DELETE` statement. The `WHERE` clause specifies which record(s) should be deleted. If you omit the `WHERE` clause, all records in the table will be deleted!

<a id="org02b14f7"></a>

## Demo Database

Below is a selection from the "Customers" table in the Northwind sample database:

![img](/img/db-table.png)

<a id="orgdaafb3f"></a>

## SQL DELETE Example

The following SQL statement deletes the customer "Alfreds Futterkiste" from the "Customers" table:

**Example**

``` sql
DELETE FROM Customers WHERE CustomerName='Alfreds Futterkiste';
```

The "Customers" table will now look like this:

![img](/img/db-table8.png)

<a id="org4412b2e"></a>

## Delete All Records

It is possible to delete all rows in a table without deleting the table. This means that the table structure, attributes, and indexes will be intact:

**Syntax**

``` sql
DELETE FROM table_name;
```

The following SQL statement deletes all rows in the "Customers" table, without deleting the table:

**Example**

``` sql
DELETE FROM Customers;
```

<a id="org73887db"></a>

# SELECT TOP

<a id="org66f038e"></a>

## The SQL SELECT TOP Clause

The `SELECT TOP` clause is used to specify the number of records to return.

The `SELECT TOP` clause is useful on large tables with thousands of records. Returning a large number of records can impact performance.

> :book: **Note**: Not all database systems support the `SELECT TOP` clause, MySQL supports the `LIMIT` clause to select a limited number of records.

**MySQL Syntax**:

``` sql
SELECT column_name(s)
FROM table_name
WHERE condition
LIMIT number;
```

<a id="orgb6abce3"></a>

## Demo Database

Below is a selection from the "Customers" table in the Northwind sample database:

![img](/img/db-table.png)

<a id="orgccd8f64"></a>

## SQL, TOP, LIMIT, and FETCH FIRST Examples

The following SQL statement selects the first three records from the "Customers" table.

**Example**

``` sql
SELECT TOP 3 * FROM Customers;
```

The following SQL statement shows the equivalent example for MySQL:

**Example**

``` sql
SELECT * FROM Customers LIMIT 3;
```

<a id="org04c2558"></a>

## SQL TOP PERCENT Example

The following SQL statement selects the first 50% of the records from the "Customers" table.

**Example**

``` sql
SELECT TOP 50 PERCENT * FROM Customers;
```

<a id="orga2b2c36"></a>

## ADD a WHERE CLAUSE

The following SQL statement selects the first three records from the "Customers" table, where the country is "Germany".

**Example**

``` sql
SELECT TOP 3 * FROM Customers WHERE Country='Germany';
```

The following SQL statement shows the equivalent example for MySQL:

**Example**

``` sql
SELECT * FROM Customers WHERE Country='Germany' LIMIT 3;
```

<a id="org27dc513"></a>

# MIN and MAX

<a id="org96fbfec"></a>

## The SQL MIN() and MAX() Functions

The `MIN()` function returns the smallest value of the selected column.

The `MAX()` function returns the largest value of the selected column.

**MIN() Syntax**

``` sql
SELECT MIN(column_name) FROM table_name WHERE condition;
```

**MAX() Syntax**

``` sql
SELECT MAX(column_name) FROM table_name WHERE condition;
```

<a id="orge006f89"></a>

## Demo Database

Below is a selection from the "Products" table in the Northwind sample database:

![img](/img/db-table9.png)

<a id="orged4e082"></a>

## MIN() Example

The following SQL statement finds the price of the cheapest product:

**Example**

``` sql
SELECT MIN(Price) as SmallestPrice FROM Products;
```

<a id="org273cf00"></a>

## MAX() Example

The following SQL statement finds the price of the most expensive product:

**Example**

``` sql
SELECT MAX(Price) as LargestPrice FROM Products;
```

<a id="orgfa0dc0f"></a>

# COUNT, AVG, SUM

<a id="orgbf3562c"></a>

## The SQL COUNT(), AVG(), and SUM() Functions

The `COUNT()` function returns the number of rows that matches a specified criterion.

**COUNT() Syntax**:

``` sql
SELECT COUNT(column_name) FROM table_name WHERE condition;
```

The `AVG()` function returns the average value of a numeric column.

**AVG() Syntax**:

``` sql
SELECT AVG(column_name) FROM table_name WHERE condition;
```

**SUM() Syntax**

``` sql
SELECT SUM(column_name) FROM table_name WHERE condition;
```

<a id="orgd9a2194"></a>

## Demo Database

Below is a selection from the "Products" table in the Northwind sample database:

![img](/img/db-table9.png)

<a id="orgdf7e29e"></a>

## COUNT() Example

The following SQL statement finds the number of products:

**Example**

``` sql
SELECT COUNT(ProductID) FROM Products
```

> :book: **NOTE**: NULL values are not counted.

<a id="org4571eba"></a>

## AVG() Example

The following SQL statement finds the average price of all products:

**Example**

``` sql
SELECT AVG(Price) FROM Products;
```

> :book: **NOTE**: NULL values are ignored.

<a id="org26d6180"></a>

## Demo Database

Below is a selection from the "OrderDetails" table in the Northwind sample database:

![img](/img/db-table10.png)

<a id="org436917f"></a>

## SUM() Example

The following SQL statement finds the sum of the "Quantity" fields in the "OrderDetails" table:

**Example**

``` sql
SELECT SUM(Quantity) FROM OrderDetails;
```

> :book: **Note**: NULL values are ignored.

<a id="orgba1eeeb"></a>

# LIKE

<a id="org6e80b8d"></a>

## The SQL LIKE Operator

The `LIKE` operator is used in a `WHERE` clause to search for a specified pattern in a column.

There are two wildcards often used in conjunction with the `LIKE` operator:

- The percent sign (%) represents zero, one, or multiple characters
- The underscore sign (\_) represents one, single character

The percent sign and the underscore can also be used in combinations!

**LIKE Syntax**

``` sql
SELECT column1, column2, ...
FROM table_name
WHERE columnN LIKE pattern;
```

> :bulb: **Tip**: You can also combine any number of conditions using `AND` or `OR` operators.

Here are some examples showing different `LIKE` operators with '%' and '\_' wildcards:

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left"><b>LIKE Operator</b></th>
<th scope="col" class="org-left"><b>Description</b></th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">WHERE CustomerName LIKE 'a%'</td>
<td class="org-left">Finds any value that starts "a"</td>
</tr>


<tr>
<td class="org-left">WHERE CustomerName LIKE '%a'</td>
<td class="org-left">Finds any value that ends "a"</td>
</tr>


<tr>
<td class="org-left">WHERE CustomerName LIKE '%or%'</td>
<td class="org-left">Finds any values that have "or" in any position</td>
</tr>


<tr>
<td class="org-left">WHERE CustomerName LIKE '<sub>r</sub>%'</td>
<td class="org-left">Finds any value that have "r" in the second position</td>
</tr>


<tr>
<td class="org-left">WHERE CustomerName LIKE 'a_%'</td>
<td class="org-left">Finds any value that start with "a" and are at least 2 characters length</td>
</tr>


<tr>
<td class="org-left">WHERE CustomerName LIKE 'a__%'</td>
<td class="org-left">Finds any values that start with "a" and are at least 3 characters length</td>
</tr>


<tr>
<td class="org-left">WHERE ContactName LIKE 'a%o'</td>
<td class="org-left">Finds any values that start with "a" and ends with "o"</td>
</tr>
</tbody>
</table>


<a id="orgfcd4c14"></a>

## Demo Database

The table below shows the complete "Customers" table from the Northwind sample database:

![img](/img/db-table11.png)

<a id="org021a981"></a>

## SQL LIKE Examples

The following SQL statement selects all customers with a CustomerName starting with "a":

**Example**

``` sql
SELECT * FROM Customers WHERE CustomerName LIKE 'a%';
```

The following SQL statement selects all customers with a CustomerName ending with "a":

**Example**

``` sql
SELECT * FROM Customers WHERE CustomerName LIKE '%a';
```

The following SQL statement selects all customers with a CustomerName that have "or" in any position:

**Example**

``` sql
SELECT * FROM Customers WHERE CustomerName LIKE '%or%';
```

The following SQL statement selects all customers with a CustomerName that have "r" in the second position:

**Example**

``` sql
SELECT * FROM Customers WHERE CustomerName LIKE '_r%';
```

The following SQL statement selects all customers with a CustomerName that starts with "a" and are at least 3 characters in length:

**Example**

``` sql
SELECT * FROM Customers WHERE CustomerName LIKE 'a__%';
```

The following SQL statement selects all customers with a ContactName that starts with "a" and ends with "o":

**Example**

``` sql
SELECT * FROM Customers WHERE ContactName LIKE 'a%o';
```

The following SQL statement selects all customers with a CustomerName that does NOT start with "a":

**Example**

``` sql
SELECT * FROM Customers WHERE CustomerName NOT LIKE 'a%';
```

<a id="org299a469"></a>

# Wildcards

<a id="orgd127ce7"></a>

## SQL Wildcard Characters

A wildcard character is used to substitute one or more characters in a string.

Wildcard characters are used with the `LIKE` operator. The `LIKE` operator is used in `WHERE` clause to search for a specified pattern in a column.

**Wildcard Characters in SQL Server**

![img](/img/db-table12.png)

All the wildcards can also be used in combinations!

Here are some examples showing different `LIKE` operators with '%' and '\_' wildcards:

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left"><b>LIKE Operator</b></th>
<th scope="col" class="org-left"><b>Description</b></th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">WHERE CustomerName LIKE 'a%'</td>
<td class="org-left">Finds any values that starts with "a"</td>
</tr>


<tr>
<td class="org-left">WHERE CustomerName LIKE '%a'</td>
<td class="org-left">Finds any value that ends with "a"</td>
</tr>


<tr>
<td class="org-left">WHERE CustomerName LIKE '%or%'</td>
<td class="org-left">Finds any values that have "or" in any position</td>
</tr>


<tr>
<td class="org-left">WHERE CustomerName LIKE '<sub>r</sub>%'</td>
<td class="org-left">Finds any values that have "r" in the second position</td>
</tr>


<tr>
<td class="org-left">WHERE CustomerName LIKE 'a__%'</td>
<td class="org-left">Finds any values that starts with "a" and are at least 3 characters in length</td>
</tr>


<tr>
<td class="org-left">WHERE ContactName LIKE 'a%o'</td>
<td class="org-left">Finds any values that starts with "a" and ends with "o"</td>
</tr>
</tbody>
</table>


<a id="orgaf9f6b8"></a>

## Demo Database

The table below shows the complete "Customers" table from the Northwind sample database:

![img](/img/db-table11.png)

<a id="org659c183"></a>

## Using the % Wildcard

The following SQL statement selects all customers with a City starting with "ber":

**Example**

``` sql
SELECT * FROM Customers WHERE City LIKE 'ber%';
```

The following SQL statement selects all customers with a City containing the pattern "es":

**Example**

``` sql
SELECT * FROM Customers WHERE City LIKE '%es%';
```

<a id="org7759167"></a>

## Using the \_ Wildcard

The following SQL statement selects all customers with a City starting with any character, followed by "ondon":

**Example**

``` sql
SELECT * FROM Customers WHERE City LIKE '_ondon';
```

The following SQL statement selects all customers with a City starting with "L", followed by any character, followed by "n", followed by any character, followed by "on":

**Example**

``` sql
SELECT * FROM Customers WHERE City LIKE 'L_n_on';
```

<a id="org5143e9c"></a>

## Using the [charlist] Wildcard

The following SQL statement selects all customers with a City starting with "b", "s", or "p":

**Example**

``` sql
SELECT * FROM Customers WHERE City LIKE '[bsp]%';
```

The following SQL statement selects all customers with a City starting with "a", "b", "c":

**Example**

``` sql
SELECT * FROM Customers WHERE City LIKE '[a-c]%';
```

<a id="org3c677ad"></a>

## Using the [!charlist] Wildcard

The two following SQL statements selects all customers with a City NOT starting with "b", "s", or "p":

**Example**

``` sql
SELECT * FROM Customers WHERE City LIKE '[!bsp]%';
```

OR

**Example**

``` sql
SELECT * FROM Customers WHERE City LIKE '[bsp]%';
```

<a id="org331a045"></a>

# IN

<a id="org7e307a4"></a>

## The SQL IN Operator

The `IN` operator allows you to specify multiple values in a `WHERE` clause.

The `IN` operator is a shorthand for multiple `OR` conditions.

**IN Syntax**

``` sql
SELECT column_name(s) FROM table_name WHERE column_name IN (value1, value2, ...);
```

**OR**

``` sql
SELECT column_name(s) FROM table_name WHERE column_name IN (SELECT STATEMENT);
```

<a id="org3912710"></a>

## Demo Database

The table below shows the complete "Customers" table from the Northwind sample database:

![img](/img/db-table11.png)

<a id="orgbf2b762"></a>

## IN Operator Examples

The following SQL statement selects all customers that are located in "Germany", "France" or "UK":

**Example**

``` sql
SELECT * FROM Customers WHERE Country IN ('Germany', 'France', 'UK');
```

The following SQL statement selects all customers that are NOT located in "Germany", "France" or "UK":

**Example**

``` sql
SELECT * FROM Customers WHERE Country NOT IN ('Germany', 'France', 'UK');
```

The following SQL statement selets all customers that are from the same countries as the suppliers:

**Example**

``` sql
SELECT * FROM Customers WHERE Country IN (SELECT Country FROM Suppliers);
```

<a id="org9ea4fcd"></a>

# BETWEEN

<a id="org4f75bae"></a>

## The SQL BETWEEN Operator

The `BETWEEN` operator selects values within a given range. The values can be numbers, text, or dates.

The `BETWEEN` operator is inclusive: begin and end values are included.

**BETWEEN Syntax**

``` sql
SELECT column_name(s) FROM table_name WHERE column_name BETWEEN value1 AND value2;
```

<a id="orgc35dae0"></a>

## Demo Database

Below is a selection from the "Products" table in the Northwind sample database:

![img](/img/db-table13.png)

<a id="orgec8bb3a"></a>

## BETWEEN Example

The following SQL statement selects all products with a price between 10 and 20:

**Example**

``` sql
SELECT * FROM Products WHERE Price BETWEEN 10 AND 20;
```

<a id="orgeb25e60"></a>

## NOT BETWEEN Example

To display the product outside the range of the previous example, use `NOT BETWEEN`:

**Example**

``` sql
SELECT * FROM Products WHERE Price NOT BETWEEN 10 AND 20;
```

<a id="org319087e"></a>

## BETWEEN with IN Example

The following SQL statement selects all products with a price between 10 and 20. In addition; do not show products with a CategoryID of 1,2, or 3:

**Example**

``` sql
SELECT * FROM Products WHERE Price BETWEEN 10 AND 20 AND CategoryID NOT IN (1,2,3);
```

<a id="org1b8c652"></a>

## BETWEEN Text Values Example

The following SQL statement selects all products with a ProductName between Carnarvon Tigers and Mozzarella di Giovanni:

**Example**

``` sql
SELECT * FROM Products WHERE ProductName BETWEEN 'Carnarvon Tigers' AND 'Mozzarella di Giovanni' ORDER BY ProductName;
```

The following SQL statement selects all products with a ProductName between Carnarvon Tigers and Chef Anton's Cajun Seasoning:

**Example**

``` sql
SELECT * FROM Products WHERE ProductName BETWEEN "Carnarvon Tigers" AND "Chef Anton's Cajun Seasoning" ORDER BY ProductName;
```

<a id="org6dd98ec"></a>

## NOT BETWEEN Text Values Example

The following SQL statement selects all products with a ProductName not between Carnarvon Tigers and Mozzarella di Giovanni:

**Example**

``` sql
SELECT * FROM Products WHERE ProductName NOT BETWEEN 'Carnarvon Tigers' AND 'Mozzarella di Giovanni' ORDER BY ProductName;
```

<a id="org319b1a2"></a>

## Sample Table

Below is a selection from the "Orders" table in the Northwind sample database:

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-right" />

<col  class="org-right" />

<col  class="org-right" />

<col  class="org-left" />

<col  class="org-right" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-right"><b>OrderID</b></th>
<th scope="col" class="org-right"><b>CustomerID</b></th>
<th scope="col" class="org-right"><b>EmployeeID</b></th>
<th scope="col" class="org-left"><b>OrderDate</b></th>
<th scope="col" class="org-right"><b>ShipperID</b></th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-right">10248</td>
<td class="org-right">90</td>
<td class="org-right">5</td>
<td class="org-left">7/4/1996</td>
<td class="org-right">3</td>
</tr>


<tr>
<td class="org-right">10249</td>
<td class="org-right">81</td>
<td class="org-right">6</td>
<td class="org-left">7/5/1996</td>
<td class="org-right">1</td>
</tr>


<tr>
<td class="org-right">10250</td>
<td class="org-right">34</td>
<td class="org-right">4</td>
<td class="org-left">7/8/1996</td>
<td class="org-right">2</td>
</tr>


<tr>
<td class="org-right">10251</td>
<td class="org-right">84</td>
<td class="org-right">3</td>
<td class="org-left">7/8/1996</td>
<td class="org-right">1</td>
</tr>


<tr>
<td class="org-right">10252</td>
<td class="org-right">76</td>
<td class="org-right">4</td>
<td class="org-left">7/10/1996</td>
<td class="org-right">2</td>
</tr>
</tbody>
</table>


<a id="org27c8445"></a>

## BETWEEN Dates Example

The following SQL statement selects all orders with an OrderDate between '01-July-1996' and '31-July-1996':

**Example**

``` sql
SELECT * FROM Orders WHERE OrderDate BETWEEN #07/01/1996# AND #07/31/1996#;
```

OR:

**Example**

``` sql
SELECT * FROM Orders WHERE OrderDate BETWEEN '1996-07-01' AND '1996-07-31';
```
