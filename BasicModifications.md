# SQL Server Basic Modification Notes
-------------------------------------
## Different Categories of SQL statments
----------------------------------------
+ Data Definiton Language
+ Data Control Language
+ Data Modification Language

## Table metadata
-----------------
+ relationships between tables should be understood
+ stored procedures and system catalogs can be used to learn more about a table
+ be aware of triggers that might cause surprise side effects to your data modifications 

## Using sp_help
----------------

+ sp_help[[@objname]'name'] 
+ sp's can be used to return an objects metadata
+ requires public role membership and at least one permission granted on table
+ also need VIEW DEFINITION permission required for seeing constraint references


+ For tables, sp_help returns(abridge):
    Column name
    Data type
    computed(yes/no)
    Length,precision,scale
    Nullability(yes/no)
    Collation

 + sp_help returns automatically-incrementing idendity columns
     column name
     seed value
     increment value
     "Not for Replication" property (true/false)

 + also includes information on GUID (rowguidcol global unique identifier) column information

## Constraint sp_help Information
---------------------------------

+ Type of constraint
+ Constraint name
+ Delete action for foreign key constraints
+ Update action " "
+ Constraint status (enabled, disabled, N/A) for check or foreign key
+ Status for replication
+ Constrait key columns



