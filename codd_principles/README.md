## Codd's 12 rules:
Dr. Edgar Frank Codd was a computer scientist, while working on IBM he invented relational model for database management which eventually led to relational database. Dr. Edgar Frank Codd proposed 12 rules and said if a database follows all these rules only and only then that database can be called a relational database management system.  
Although all the relational database management systems should follow these rules, hardly any database in the market follows all the rules.    

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

### RULE 4 (Active online catalog):
This rule states that the structure description of whole database must be stored in an online catalog, i.e. data dictionary, which can be accessed by the authorized users. The Catalog must be governed by the same rules as rest of the database. Users can use the same query language to access the catalog which they use to access the database itself.

### RULE 5 (Comprehensive data sub-language rule):
This rule states that a database must have a support for a language which has linear syntax which is capable of data definition, data manipulation and transaction management operations. Database can be accessed by means of this language only, either directly or by means of some application. If the database can be accessed or manipulated in some way without any help of this language, it is then a violation.  
For example SQL language is used in MySQL database.

### RULE 6 (View updating rule):
All the view that are theoretically updatable should be updatable by the system as well.

### RULE 7 (High-level insert, update and delete rule):
This rule states the database must employ support high-level insertion, updation and deletion. This must not be limited to a single row that is, it must also support union, intersection and minus operations to yield sets of data records.

### RULE 8 (Physical data independence):
This rule states that the application should not have any concern about how the data is physically stored. Also, any change in its physical structure must not have any impact on application.  
For example if a file supporting table is moved from one disk to another, it shouldn't affect the application.

### RULE 9 (Logical data independence):
This rule states that the logical data must be independent of its user’s view (application). Any change in logical data must not imply any change in the application using it. For example, if two tables are merged or one is split into two different tables, there should be no impact or change on user application. This is one of the most difficult rule to apply.

### RULE 10 (Integrity independence):
This rule states that the database must be independent of the application using it. All its integrity constraints can be independently modified without the need of any change in the application. This rule makes database independent of the front-end application and its interface.

### RULE 11 (Distribution independence):
This rule states that the end user must not be able to see that the data is distributed over various locations. User must see that the data is located at one site only. This rule has been proven as a foundation of distributed database systems.

### RULE 12 (Non-subversion rule):
This rule states that if a system has an interface that provides access to low level records, this interface then must not be able to subvert the system and bypass security and integrity constraints to change the data. This can be achieved by some kind of encryption.


Some of these rules are very hard to achieve and some are pratically very difficult to apply in a market application.








