# SQL_query

Structured query language (SQL) is a programming language for storing and processing information in a relational database.

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


## SELECT  rows from a specific table by LIMIT

- Syntax

  SELECT * FROM table_name LIMIT id_number;

- Example

  SELECT * FROM customer LIMIT 5;

***NOTE***:

in this way SELECT * FROM table_name LIMIT id_number; we will get the value till id_number

## SELECT with where condition

- Syntax
  
  SELECT * FROM table_name WHERE column_name < number;

  SELECT * FROM table_name WHERE column_name > number;

  SELECT * FROM table_name WHERE column_name <= number;

  SELECT * FROM table_name WHERE column_name = number AND column_name = number

  SELECT * FROM table_name WHERE column_name = number OR column_name = number;

- Example

  SELECT * FROM albums Where release_year < 2000;

  SELECT * FROM albums WHERE release_year = 1819 AND brand_id = 1; 

  ***NOTE***:
  amar albums table ar release_year column ar moddhe 2000 ar niche je data ba value gulo ache ta show korbe 

  amar albums table ar release_year name aaa je field ache oi fild ar moddhe 1819 name kono value thakle abong brand_id field ta jodi tar 1 hoy tahole data show korbe  


## SELECT with BETWEEN (it works like filter) 

  if you want to filtering your specific table specific column then you can use it.

* Syntax

  SELECT * FROM table_name WHERE column_name BETWEEN  minimum_value AND maximum_value;

  SELECT * FROM table_name WHERE column_name IS NULL;

* Example

  SELECT * FROM albums WHERE release_date BETWEEN 2000 and 2002;

  SELECT * FROM albums WHERE release_date IS NULL;

***NOTE***:

akhane amar albums table ar release_date field theke BETWEEN filtering korbe je oi field ar moddhe 2000 theke 2002 porjonto koto gulo record ba value ache abong she shei gulo dekhabe

jodi amar albums table ar release_date column ar kono value NULL thake tahole shei row ta dekhabe
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

## For watching all Databases 

[Tutorial Link](https://www.youtube.com/watch?v=Tdl7CGnhPeA)

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


## For deleting database

- Syntax

  drop database database_name;

- Example
  
  drop database User;
## For creating a new table

* Syntax

  create table table_name(field_name type(length) , field_name type(length) , ...............);

* Example

  create table userinfo(name varchar(30) ,Address varchar(50), id int not null primary key);

  Note:if you create your table in this way then your id collumn will be create at last of the row 


## For deleting a table

- Syntax

  drop table table_name;

- Example

  drop table userinfo;

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


# sum() , avg() , min() ,max() and count() this 5 functions are called aggregatefunction

  ##  For sum a specific collumn of a specific table
    you can  addition of a specific collumn value 

  * Syntax

    select sum(collumn_name)from table_name;

  * Example

    select sum(salary)from userinfo;

  ##  For avrage a specific collumn of a specific table  

  * Syntax

    select avg(collumn_name) from table_name;

  * Example

    select avg(salary) from userinfo;

  ##  For counting total number of raws of a specific table

  * Syntax

    select count(collumn_name) from table_name;

  * Example

    select count(id) from userinfo;
  
  ## For find out a maximum value of a specific collumn from a specific table

  * Syntax

    select max(collumn_name) from table_name;

  * Example

    select max(salary) from userinfo;

## For find out a minimum value of a specific collumn from a specific table

  * Syntax

    select min(collumn_name) from table_name;

  * Example

    select min(salary) from userinfo;

## For assending and descending our collumn value we can use order by

### 1.assending  

  it will show lower to higher format 

* Syntax

  select * from table_name order by collumn_name;

* Example

  select * from userinfo order by salary;

  Note: it will show assending(means lower to higher) format bydefault

### 2.descending

  it will show higher to lower format

* Syntax

  select * from table_name order by collumn_name desc;

* Example

  select * from userinfo order by salary desc;

## For finding a specific vale of a specific collumn from a specific table  

* Syntax

  select * from table_name where collumn_name like 'starting_letter%';

* Example

  select * from userinfo where name like 'd%' ;

  Note: it will find my userinfo table name field valu and it will also  chack which value start with d  . it's not case-sensitive and % means it will access many alphabets and '_%' or '%_' or '% %' colled whiled card

### Or

  if you want to chack by specific collunm values last letter

* Syntax

  select * from table_name where collumn_name like '%Ending_letter';


* Example

  select * from userinfo where name like '%a';

  Note: it will find my userinfo table name field valu and it will also  chack which value End with a  . it's not case-sensitive

### Or

  if you want to chack by specific collunm values Second letter

* Syntax

  select * from table_name where collumn_name like '_Second letter%';


* Example

  select * from userinfo where name like '_n%';

  Note: it will find my userinfo table name field valu and it will also  chack Second value with n  . it's not case-sensitive
   

### Or

  if you want to chack by specific collunm values Second last letter

* Syntax

  select * from table_name where collumn_name like '%Second letter_';


* Example

  select * from userinfo where name like '%n_';

  Note: it will find my userinfo table name field valu and it will also  chack Second last value with n  . it's not case-sensitive

### Or

  if you want to chack by specific collunm values Middle letter

* Syntax 

  select * from table_name where column_name like '%Middle letter %';

* Example

  select * from albums where name like '%i%';  
## Join  

 we need two tables

* Syntax

  SELECT * FROM table_name JOIN table_name ON table1_common_field = table2_common_field

* Example

  SELECT * FROM userinfo JOIN employe ON userinfo.id = employe.id

***NOTE***:

join   r  inner join akoi

### Inner join

which will be common between two tables only that will be accessable

- Syntax
  
  select * from table1_name inner join table2_name on table1_common_field = table2_common_field;

- Example

  select * from userinfo inner join employe on userinfo.id =  employe.id;

  ***Note*** : 
  
  So here i have used both table id collumn to join two table and id collumn is common in both table. if id number is same in two tables then I will only be able to see thoes id's all records. In this way we can join 2 tables together



### Left join

- Syntax

  select * from table1_name left join table2_name on table1_common_field = table2_common_field; 

- Example

  select * from userinfo left join employe on userinfo.id = togetheremploye.id;  
  
  ***Note***:

  left join ar bam pashe je table ta thakbe she table ar sob element ashbe kintu left join ar dan pashe je table ta thakbe oita jodi bam pasher table ar sahte match na kore tahoe null value return korbe
### Right join

- Syntax

  select * from table1_name right join table2_name on table1_common_field = table2_common_field;


- Example  

  select * from userinfo right join employe on userinfo.id = employe.id;

  ***Note***:

  right join ar dan pashe je table ta thakbe she table ar sob element ashbe kintu right join ar bam pashe je table ta thakbe oita jodi dan pasher table ar sahte match na kore tahoe null value return korbe

### Cross join

  in Cross join no need to write any condition

 - Syntax

  select * from table1_name cross join table2_name;

 - Example

  select * from userinfo cross join ;

 ***Note***:

  cross join ar bam side ar table ar ak ak ta row dan side ar tabel ar sob gulo row ar sathe relation generate kore jemon prothom 1st table ar 1st row 2nd table ar sobar sathe abar 1st table ar 2nd row 2nd table ar sob sobar sathe relation generate kore. jodi amar akta table a 5 ta rows thake abong onno table a 6 ta rows thake tahole ai 2ta table a jodi ami cross join kori tahole total rows hobe 5*6=30 ta. cross join ke  beshi use kora hoy na. 

  cross join amra tokhon ee bebohar kori jokhon amader emon dhoroner data ante hobe jekhane 2 ta table aksathe data niye ashbe abong protita table onno table ar sathe akta multiple relation generate korbe tokhon.




# Tutorial 2 

[Link](https://www.youtube.com/watch?v=p3qvj9hO_Bo)

## Foreign key 

- Example

  create table brands(
  id int not null auto_increment primary key,
  name varchar(100) not null    
  );

  create table albums(
  id int not null auto_increment primary key,
  name varchar(100) not null,
  relese_year int,
  brand_id int not null,
  foreign key (brand_id) references brands(id)   
  );

## Distinct 

  jodi emon hoy je amader kono table ar kono specific column ba field ar moddhe same value oonek bar ache kintu ami chachhi same value akbar ee dekhabe tokhon amra Distinct bebohar korbo.

 - Example   

  i have an albums table where i have a column which is name column and name column values are  sad,Hip-Hop,rock,pop,jazz,pop
  here as you can see pop  is 2 time .If you run this SELECT name FROM albums; you will get all values of name field if name field may have same value manytime then you will get same value manytime.
  
  if you run SELECT DISTINCT name FROM albums;
  you will get all value of name field. Help of DISTINCT you will naver get same value again and again.


## GROUP BY  

  [Link](https://www.youtube.com/watch?v=apNmMWgFFRg)

  jodi emon hoy je amader ekta employ table ache jar moddhe dhoro employId,employName,depeartment,salary . akhon amar department column ar moddhe oonek department ar nam thakte pare jemon Technology,Marketing,Production,Management and so on.abong akoi department name oonek bar thakte pare ...akhon jodi bola hoy amar kon department a koto jon lok ache tokhon ai data ta pawar jonno amader GROUP BY ar concept a ashte hobe karon ai ta WHERE diye possiable na.    

  * Syntax

    SELECT group_by_ar_sathe_je_column_ar_nam_thakbe,aggregatefunction(collumn_name othoba * ) FROM table_name GROUP BY column_name; 


  * Example

    SELECT depeartment,count(*) FROM employe GROUP BY depeartment; 


  ***NOTE***:
  aggregate function mot 5 ta sum(), avg(), min(), max(), count() 
