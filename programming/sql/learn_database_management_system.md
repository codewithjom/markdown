# :point_right: Learn Database Management System

## Table of Contents

- [Introduction of DBMS (Database Management System) | Set 1](#org5256d68)
  - [Data Manipulation Language (DML)](#orgdf9b636)
  - [Data Control Language (DCL)](#org1632e49)
  - [Database Management System (DBMS)](#org86d1a99)
  - [Paradigm Shift from File System to DBMS](#org8ebcd5a)

<a id="org5256d68"></a>

# Introduction of DBMS (Database Management System) | Set 1

A database is a collection of inter-related data which helps in the efficient retrieval, insertion, and deletion of data from the database and organizes the data in the form of tables, views, schemas, reports, etc. For Example, a university database organizes the data about students, faculty, admin staff, etc. which helps in the efficient retrieval, insertion, and deletion of data from it. **DDL** is the short name for Data Definition Language, which deals with database schemas and description, of how the data should reside in the database.

- `CREATE` : to create a database and its objects like (table, index, views, store procedure, function, and triggers)
- `ALTER` : alters the structure of the existing database
- `DROP` : delete objects from the database
- `TRUNCATE` : remove all records from a table, including all spaces allocated for the records are removed
- `COMMENT` : add comments to the data dictionary
- `RENAME` : rename an object

<a id="orgdf9b636"></a>

## Data Manipulation Language (DML)

**DML** is the short name for Data Manipulation Language which deals with data manipulation and includes most common SQL statements such SELECT, INSERT, UPDATE, DELETE, etc., and it is used to store, modify, retrieve, delete, and update data in a database.

- `SELECT` : retrieve data from a database
- `INSERT` : insert data into a table
- `UPDATE` : updates existing data within a table
- `DELETE` : delete all records from a database table
- `MERGE` : UPSERT operation (insert or update)
- `CALL` : call a PL/SQL or Java subprogram
- `EXPLAIN PLAN` : interpretation of the data access path
- `LOCK TABLE` : concurrency Control

<a id="org1632e49"></a>

## Data Control Language (DCL)

**DCL** is short for Data Control Language which acts as an access specifier to the database. (basically to grant and revoke permissions to users in the database)

- `GRANT` : grant permissions to the user for running DML(SELECT, INSERT, DELETE,&#x2026;) commands on the table
- `REVOKE` : revoke permissions to the user for running DML(SELECT, INSERT, DELETE,&#x2026;) command on the specified table

<a id="org86d1a99"></a>

## Database Management System (DBMS)

The software which is used to manage databases is called Database Management System(DBMS). For example, MySQL, Oracle, etc. are popular commercial DBMS used in different applications. DBMS allows users to the following tasks:

- **Data Definition** : It helps in the creation, modification, and removal of definitions that define the organization of data in the database.

- **Data Updation** : It helps in the insertion, modification, and deletion of the actual data in the database.

- **Data Retrieval** : It helps in the retrieval of data from the database which can be used by applications for various purposes.

- **User Administration** : It helps in registering and monitoring users, enforcing data security, monitoring performance, maintaining data integrity, dealing with concurrency control, and recovering information corrupted by unexpected failure.

<a id="org8ebcd5a"></a>

## Paradigm Shift from File System to DBMS

File System manages data using files on a hard disk. Users are allowed to create, delete, and update the files according to their requirements. Let us consider the example of file-based University Management System. Data of students is available to their respective Departments, Academics Section, Result Section, Accounts Section, Hostel Office, etc. Some of the data is common for all sections like Roll No, Name, Father Name, Address, and Phone number of students but some data is available to a particular section only like Hostel allotment number which is a part of the hostel office. Let us discuss the issues with this system:

- **Redundancy of data** : Data is said to be redundant if the same data is copied at many places. If a student wants to change their Phone number, he or has to get it updated in various sections. Similarly, old records must be deleted from all section representing that student.

- **Inconsistency of Data** : Data is said to be inconsistent if multiple copies of the same data do not match each other. If the Phone number is different in Accounts Section and Academics Section, it will be inconsistent. Inconsistency may be because of typing errors or not updating all copies of the same data.

- **Difficult Data Access** : A user should know the exact location of the file to access data, so the process is very cumbersome and tedious. If the user wants to search the student hostel allotment number of a student from 10000 unsorted student's records, how difficult it can be.

- **Unauthorized Access** : File Systems may lead to unauthorized access to data. If a student gets access to a file having his marks, he can change it in an unauthorized way.

- **No Concurrent Access** : The access of the same data by multiple users at the same time is known as concurrency. The file system does not allow concurrency as data can be accessed by only one user at a time.

- **No Backup and Recovery** : The file system does not incorporate any backup and recovery of data if a file is lost or currupted.

