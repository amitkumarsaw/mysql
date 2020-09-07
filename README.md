# MySQL:

- SQL: Structured Query Language
- MySQL: "My" is the daughter’s name of the MySQL’s co-founder, "Monty Widenius". The name of MySQL is the combination of My and SQL, MySQL.

Some of you might be confused between `SQL` and `MySQL`. The difference is really simple, SQL is a database language whereas MySQL is a database software. MySQL is database software which uses "SQL" language to query the database.  

### MySQL: 

MySQL is the most popular Open Source Relational SQL Database Management System (RDBMS). MySQL is one of the best RDBMS being used for developing various web-based software applications. It is open source software backed by Oracle.  

### SQL:
SQL contains three parts:  
1. Data definition language (DDL)
1. Data manipulation language (DML)
1. Data control language (DCL)

#### Data definition language:
-> Data Definition Language (DDL) statements are used to define the database structure. Data Definition Language  describes how the data should exist in the database.  

DDL contains following commands:
- CREATE - to create objects/tables in the database
- ALTER - alters the structure of the database
- DROP - delete objects/table from the database
- TRUNCATE - remove all records from a table, including all spaces allocated for the records are removed
- COMMENT - add comments to the data dictionary
- RENAME - rename an object/table  

#### Data manipulation language:
-> Data Manipulation Language (DML) statements are used for managing data within database objects. DML deals with data manipulation and hence contains the following commands,  

- INSERT
- SELECT
- UPDATE
- DELETE

#### Data control language:
-> Data control language (DCL) allows you to grant the permissions to a user to access specific data in the database.  

It contain commands like,  
- GRANT
- REVOKE

### SHOW DATABASES command:
This command shows all the databases available in your mysql server.  

**Syntax:**
```mysql
mysql> show databases;
```

### USE command:
We use the `USE` command to select a particular database to work with.  

**Syntax:**
```mysql
mysql> USE database_name;
```

### SELECT DATABASE() command:    *NOTE: it is different than the SELECT command of DML*
To see the current database you are working on, we use `select database()` command.

**Syntax:**  
```mysql
mysql> select database();
```
### CREATE DATABASE command:
This command creates a new database for the user with a name given by the user.

**Syntax:**  
```mysql
mysql> CREATE DATABASE database_name;
```
Then we neen to use the database using the `USE` command, `use database_name;`. This will make that database the current working database.  

### DROP DATABASE command:
The DROP DATABASE statement drops all tables in the database and deletes the database permanently. Therefore, you should be very careful when using this statement.  

**Syntax:**
```mysql
mysql> DROP DATABASE database_name;
```

### 























