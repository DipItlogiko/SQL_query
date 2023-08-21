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

  SELECT collumn_name FROM table_name;

  SELECT collumn_name,collumn_name FROM table_name;

  SELECT * FROM table_name where id= id_number;

* Example

  SELECT CustName FROM customer;

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

## For watching all Databases  [Tutorial Link](https://www.youtube.com/watch?v=Tdl7CGnhPeA)

* show databases;
  
  it will show all databases name

## For create a new database

* Syntax

  create database database_name;

* Example

  create database User;

##  For use database

* Syntax

  use database_name;

* Example

  use User;

## For creating a new table

* Syntax

  create table table_name(field_name type(length) , field_name type(length) , ...............);

* Example

  create table userinfo(name varchar(30) ,Address varchar(50), id int not null primary key);

  Note:if you create your table in this way then your id collumn will be create at last of the row 

## For describing the table

   if you want to know about table then you can use the queary.And you will get  all information about the table.

* Syntax

  desc table_name;

* Example

  desc userinfo;

## For adding a new collumn in a table

* Syntax

  alter table table_name add new_collumn_name type(length);

* Example

  alter table userinfo add position varchar(50);

## For increasing field type

* Syntax

  alter table table_name modify column column_name type(length);

* Example

  alter table userinfo modify column position varchar(80);

## For removing column from a table

* Syntax

  alter table table_name drop column column_name;

* Example

  alter table userinfo drop column position;


## For deleting any row from a table

* Syntax

  delete from table_name where id= id_number;

* Example

  delete from userinfo where id=2; 

##   
