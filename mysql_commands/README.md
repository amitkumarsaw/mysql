# MySQL:

- SQL: Structured Query Language
- MySQL: "My" is the daughter’s name of the MySQL’s co-founder, "Monty Widenius". The name of MySQL is the combination of My and SQL, MySQL.

Some of you might be confused between `SQL` and `MySQL`. The difference is really simple, SQL is a database language whereas MySQL is a database software. MySQL is database software which uses "SQL" language to query the database.  

## MySQL: 

MySQL is the most popular Open Source Relational SQL Database Management System (RDBMS). MySQL is one of the best RDBMS being used for developing various web-based software applications. It is open source software backed by Oracle.  

## SQL:
SQL contains three parts:  
1. Data definition language (DDL)
2. Data manipulation language (DML)
3. Data control language (DCL)  

---  

### Data definition language:
-> Data Definition Language (DDL) statements are used to define the database structure. Data Definition Language  describes how the data should exist in the database.  

DDL contains following commands:
- CREATE - to create objects/tables in the database
- ALTER - alters the structure of the database
- DROP - delete objects/table from the database
- TRUNCATE - remove all records from a table, including all spaces allocated for the records are removed
- COMMENT - add comments to the data dictionary
- RENAME - rename an object/table  
---
### Data manipulation language:
-> Data Manipulation Language (DML) statements are used for managing data within database objects. DML deals with data manipulation and hence contains the following commands,  

- INSERT
- SELECT
- UPDATE
- DELETE  
---
### Data control language:
-> Data control language (DCL) allows you to grant the permissions to a user to access specific data in the database.  

It contain commands like,  
- GRANT
- REVOKE  

---
---

# MYSQL DATA DEFINITION :

### SHOW DATABASES :
This command shows all the databases available in your mysql server.  

**Syntax :**
```mysql
mysql> show databases;
```
---

### USING A DATABASE :
We use the `USE` command to select a particular database to work with.  

**Syntax :**
```mysql
mysql> USE database_name;
```
---

### SELECT DATABASE() :
To see the current database you are working on, we use `select database()` command.

**Syntax :**  
```mysql
mysql> select database();
```
---

### CREATE DATABASE :
This command creates a new database for the user with a name given by the user.

**Syntax :**  
```mysql
mysql> CREATE DATABASE database_name;
```

Then we neen to use the database using the `USE` command, `use database_name;`. This will make that database the current working database.   

```mysql
mysql> CREATE DATABASE [IF NOT EXISTS] database_name;
```

`IF NOT EXISTS` is an optional clause of the statement. The IF NOT EXISTS clause prevents you from an error of creating a new database that already exists in the database server.

---

### DROP DATABASE :
The DROP DATABASE statement drops all tables in the database and deletes the database permanently. Therefore, you should be very careful when using this statement.  

**Syntax :**
```mysql
DROP DATABASE database_name;
```

```mysql
DROP DATABASE [IF EXISTS] database_name;
```

---

### CREATE TABLE :
Before the `CREATE TABLE` command first look at [MySQL Data Types](https://github.com/amitkumarsaw/mysql/tree/master/mysql_datatypes).  
The `CREATE TABLE` command allows us to create a new table in an existing database.  

**Syntax :**  
```sql
CREATE TABLE [IF NOT EXISTS] table_name(
   column_1_definition,
   column_2_definition,
   …,
   table_constraints
) ENGINE=storage_engine;
```
Here we specify the name of the table that we want to create after the `CREATE TABLE` keywords. The table name must be unique within a database. The `IF NOT EXISTS` is optional. It allows us to check if the table that we create already exists in the database. If this is the case, MySQL will ignore the whole statement and will not create any new table.  

We can optionally specify the storage engine for the table in the ENGINE clause.  

**e.g. :**  
```mysql
CREATE TABLE table1
( number INT(11) AUTO_INCREMENT,
name VARCHAR(32) NOT NULL,
city VARCHAR(32),
age VARCHAR(7),
CONSTRAINT key1 PRIMARY KEY (name)
);
```
---

### PRIMARY KEY :
A primary key is a column or a set of columns that uniquely identifies each row in the table.  
A primary key column cannot have NULL values.  
A table can have one an only one primary key.  

**Syntax :**
```mysql
CREATE TABLE table_name(
    column_name1 datatype PRIMARY KEY,
    column_name2 datatype,
    ...
);
```
**e.g. :**
```mysql
CREATE TABLE users(
   id INT AUTO_INCREMENT PRIMARY KEY,
   user_name VARCHAR(20),
   pwd VARCHAR(100),
   email VARCHAR(100)
);
```

When the primary key has more than one column, you can use the PRIMARY KEY constraint as a table constraint.
```mysql
CREATE TABLE table_name(
    primary_key_column1 datatype,
    primary_key_column2 datatype,
    ...,
    PRIMARY KEY(column_list)
);
```
**e.g. :**
```mysql
CREATE TABLE roles(
   user_id INT AUTO_INCREMENT,
   role_id INT,
   user_name VARCHAR(50),
   PRIMARY KEY(role_id, user_id)
);
```
`AUTO_INCREMENT` attribute automatically generates a sequential integer whenever you insert a new row into the table.  

---

### UNIQUE constraint :
A UNIQUE constraint is an integrity constraint that ensures values in a column or group of columns to be unique.  A UNIQUE constraint can be either a column constraint or a table constraint.  
**Syntax :**
```mysql
CREATE TABLE table_name(
    column_name1 data_type,
    column_name2 data_type UNIQUE,
    ...
);
```
```mysql
CREATE TABLE table_name(
   column_name1 datatype,
   column_name2 datatype,
   ...,
   UNIQUE(column_name1,column_name2)
);
```
If you define a UNIQUE constraint without specifying a name, MySQL automatically generates a name for it. To define a UNIQUE constraint with a name, you use this syntax:
```mysql
[CONSTRAINT constraint_name]
UNIQUE(column_list)
```
**e.g. :**
```sql
CREATE TABLE student (
    student_id INT AUTO_INCREMENT,
    name VARCHAR(40) NOT NULL,
    phone VARCHAR(15) NOT NULL UNIQUE,
    address VARCHAR(40) NOT NULL,
    PRIMARY KEY (student_id),
    CONSTRAINT uc_name_address UNIQUE (name , address)
);
```
---

### NOT NULL constraint :
The NOT NULL constraint is a column constraint that ensures values stored in a column are not NULL.  
**e.g. :**
```sql
CREATE TABLE tasks (
    id INT AUTO_INCREMENT PRIMARY KEY,
    title VARCHAR(255) NOT NULL,
    start_date DATE NOT NULL,
    end_date DATE
);
```
---

### ALTER TABLE :
The ALTER TABLE ADD statement allows you to add one or more columns to a table.  
**syntax :**
```mysql
ALTER TABLE table_name
ADD 
    new_column_name column_definition
    [FIRST | AFTER column_name]
```
`[FIRST | AFTER column_name]` specifies the position of the new column.
`FIRST` is used to add the column at the start.
`AFTER` is used to add the column after an existing column.
By default mysql assigns the column the last position.

**e.g. :**
```mysql
ALTER TABLE watches
ADD model VARCHAR(100) NOT NULL;
```

#### ALTER TABLE – Modify columns : 
 
It modifies the column of the table.  
Suppose we need to change the data type of a column, we can use the `MODIFY` keyword.  
**e.g. :**
```mysql
ALTER TABLE watches
MODIFY note CHAR(100) NOT NULL;
```

#### ALTER TABLE – Rename a column in a table :
**e.g. :**
```mysql
ALTER TABLE watches
CHANGE COLUMN note description VARCHAR(100) NOT NULL;
```
`note` has been changed with `description`.

#### ALTER TABLE – Drop a column :

It is used to delete or drop a column.  

**e.g. :**
```mysql
ALTER TABLE watches
DROP COLUMN description;
```

#### ALTER TABLE – Rename table :
**e.g. :**  
```mysql
ALTER TABLE watches
RENAME TO clocks;
```
---

### DROP TABLE :

It is used to drop the entire table from a database.  

**Syntax :**
```mysql
DROP TABLE table_name;
```

### TRUNCATE TABLE :

- The `TRUNCATE TABLE` statement allows you to delete all data in a table.
- It is same as the `DELETE` statement used with `WHERE` clause to delete the data of the table. The difference is that the `TRUNCATE TABLE` deletes the whole table and then creates the table structure again instead of deleting the rows one by one.
- `TRUNCATE` is more efficient then the `DELETE` command.  

**e.g. :**
```mysql
TRUNCATE TABLE clocks;
```
---
---


# MYSQL DATA MANIPULATION :

### SELECT :

The SELECT statement allows you to read data from one or more tables.  

**Syntax :**  
```mysql
SELECT select_list FROM table_name;
```

**e.g. :**  
```mysql
SELECT std_id FROM students;
```
This will return the `std_id` column from the `students` table.
```mysql
SELECT * FROM students;
```
It will retuen all the columns in the `students` table.
```mysql
SELECT std_id, name FROM students;
```
It will return the `std_id` and `name` column from the `students` table.

---






