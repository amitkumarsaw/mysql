## Codd's 12 rules:
Dr. Edgar Frank Codd was a computer scientist, while working on IBM he invented relational model for database management which eventually led to relational database. Dr. Edgar Frank Codd proposed 12 rules and said if a database follows all these rules only and only then that database can be called a relational database management system.  
Although all the relational database management systems should follow these rules, hardly any database in the market follows all the rules. The reason is because following all these rules can make a database complicated and not so easy to access the data from it. You will be able to understand this statement more once we study all the 12 rules.  

Let's take a look at all the 12 rules one by one,  

### RULE ZERO:
For a system to be a relational database management system (RDBMS) it must use its relational abilities to manage data inside the database.

All other 12 rules were derived from this rule.

### RULE 1 (THE INFORMATION RULE):
This rule states that all information (user data or metadata), which is stored in the database, must be a value of some table cell. Everything in a database must be stored in table formats.  

*NOTE: Metadata can simply be described as data about data. Metadata provides the basic and relevant information about the data.  
Metadata functions in SQL Server return information about the database, database objects, database files, file groups etc.*  

e.g.  

`SELECT OBJECT_ID('dbo.DimEmployee') AS 'Object Id'`  

OUTPUT:  

|Object Id |
|----------|
|1133456667|

### RULE 2 (Guaranteed Access rule):
This rule states that every single data element (value) is guaranteed to be accessible logically with combination of table-name, primary-key (row value) and attribute-name (column value). No other means, such as pointers, can be used to access data.  

**Table Name + Primary Key(Row) + Attribute(column)**  

### RULE 3 (Systematic Treatment of NULL values):
This rule states the NULL values in the database must be given a systematic treatment. As a NULL may have several meanings, i.e. NULL can be interpreted as one the following: data is missing, data is not known, data is not applicable etc. It should be handled consistently. Also, Primary key must not ever be null.

### Rule 4 (Active online catalog):
This rule states that the structure description of whole database must be stored in an online catalog, i.e. data dictionary, which can be accessed by the authorized users. The Catalog must be governed by the same rules as rest of the database. Users can use the same query language to access the catalog which they use to access the database itself.

### Rule 5 (Comprehensive data sub-language rule):







