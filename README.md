# SQL_query

[TutorialLink](https://www.youtube.com/watch?v=4YAAgrm8_ZI)


## Insert Values In Table

The INSERT INTO Statement is used to insert new records in a table

* Syntax

INSERT INTO table_name
(column1,column2,column3,............columnN)
VALUES
(value1,value2,value3,........valueN);

* Example

INSERT INTO customer

(CustID , CustName , Age, City ,Salary)

VALUES

(1, 'Anik' , 20 , 'Dhaka' , 9000),
(2, 'Ashik' , 25 , 'Jessore' , 10000),
(3, 'Puja' , 35 , 'Faridpur', 12000);

## SELECT All Records from Specific Table
* Syntax

SELECT * FROM table_name

* Example

SELECT * FROM customer

## SELECT a specific collumn of a specific table

* Syntax

SELECT collumn_name FROM table_name

* Example

SELECT CustName FROM customer

## Update Values In Table

The UPDATE command is used to update existing rows in a table 

* Syntax

UPDATE table_name

SET "Column_name1" = 'value1' , "Column_name2"= 'value2'

WHERE "id"= 'value';

* Example

UPDATE customer

SET CustName='Priya' ,Age=35

WHERE CustID=1;

## Delete Values In Table

The DELETE statement is used to delete existing records in a table

* Syntax

DELETE FROM table_name

WHERE condition;

* Example

DELETE FROM customer

WHERE CustID=1;

