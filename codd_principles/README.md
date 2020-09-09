## Codd's 12 rules:
Dr. Edgar Frank Codd was a computer scientist, while working on IBM he invented relational model for database management which eventually led to relational database. Dr. Edgar Frank Codd proposed 12 rules and said if a database follows all these rules only and only then that database can be called a relational database management system.  
Although all the relational database management systems should follow these rules, hardly any database in the market follows all the rules. The reason is because following all these rules can make a database complicated and not so easy to access the data from it. You will be able to understand this statement more once we study all the 12 rules.  

Let's take a look at all the 12 rules one by one,  

### RULE ZERO:
For a system to be a relational database management system (RDBMS) it must use its relational abilities to manage data inside the database.

All other 12 rules were derived from this rule.

### RULE 1 (THE INFORMATION RULE):
This rule states that all information (user data or metadata), which is stored in the database, must be a value of some table cell. Everything in a database must be stored in table formats.  

*NOTE: Metadata can simply be described as data about data. Metadata provides the basic and relevant information about the data. Metadata functions in SQL Server return information about the database, database objects, database files, file groups etc.  
e.g.  
`SELECT OBJECT_ID('dbo.DimEmployee') AS 'Object Id'*

