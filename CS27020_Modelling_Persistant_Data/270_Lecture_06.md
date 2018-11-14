# CS27020 Lecture 6 - SQL  
__Thursday, October 12th 2017__  
Lecture: hmd1@aber.ac.uk   
Notes: ela12@aber.ac.uk

## History and Background 

Originally called "Sequel" - Structured English Query Language was an IBM Project in the 70's. However, 'sequel' was trademarked so it became SQL - Strcutred Query Language. 
An ANSI standard exsists for the language, with most systems _nearly_ interoperable, and so SQL is fairly portable. 

SQL incorporates three sub-languages: 

- Data Definition Language
	- 
- Data Manipulation Language
 	- Updates, selects, joins, etc.
- Data Control Language
	- Control access to the DB - who can do what.

### SQL v DB Theoretic Models

In an SQL context, a 'relation' (RDM terminology) is called a 'table'. SQL tables are:   
- Lists of rows 
- The order of rows can be used in queries 
- There are NULLS

### SQL Conventions 

SQL commands are not case sensitive. It's conventional to put SQL termins in CAPITALS in order to make them stand out. Table and attribute names in SQL _are_ case sensitive. 

### SQL Syntax 

Strings in SQL are surrounded by single quotes: 

`'I AM A STRING'`

Single quotes within a string are doubles/escaped using" 

`'I''M A STRING'`

`''` is an empty string. 

> It is difficult to truly learn about a language just through lectures - it's like learning to ride a bike by reading a book. Therefore it is useful to practically learn SQL - try [SQL on Codecadeny](https://www.codecademy.com/courses/learn-sql) 

## Data Definition Language

### Creating Tables 

```sql
CREATE TABLE tableName {
	column1Name column1Specification
	column1Name column2Specification
	...
}
```

#### Example

```sql 
CREATE TABLE fruits {
	fruitName VARCHAR(20),
	fruitPrice INT,
	...
}
```

### Types 

IN SQ the types of things you can store follow the kinds of datatypes you already know: 
`int` `float` `char` 

> TODO - Write in table of different datatypes and RDBMS systems. 

Some types are DB specific. For example, some RDBMS have ENUM enumerated types, others let you define them, others don't let you define them so you have to 'hack' them together with tables. 

### Column Definitions and Constraints 

To maintain data integrity, we can specify that attributes are not NULL. 

From our earlier example: 

```sql
CREATE TABLE fruits {
	fruitName VARCHAR(20) NOT NULL.,
	fruitPrice INT DEFAULT 20,
	...
}
``` 

### Column Contraints and Uniqueness 

...
...

####Keys as Column Contraints

```sql
CREATE TABLE ... do some writing of some coding please. 
```

#### Foreign Keys as Column Constraints

Data definitions have a lot to do with data integrity: 
 - We can restrict types of data....

 
### Other Commands in Data Definition Language 

#### Deleteing Tables

```sql
DROP TABLE fruits
``` 

These need to be used carefully - sometimes it is impossible to undo data removal. 

## Selecting 

Selecting items from a table is fairly straightforwards. In the below example of a table of fruits:

```sql
SELECT fruitName FROM fruits 
```

### Ordering Results 

```sql
SELECT fruitName FROM fruits ORDER BY price // Not returning the price, just ordering the results using their price. 
```
### Selecting All
```sql
SELECT * FROM fruits
```

### Selection of an entire row or rows

```sql
SELECT * FROM fruits WHERE fruitName = 'Pear'
```

`WHERE` restrictions can take several types: 

- Inequalities ( <, >, <=, >=)
- Equalities
- Logical Operators (`AND` `OR` `NOT`)

### Summary of `SELECT` clause 

```sql
SELECT 
	[DISTINCT | ALL] <columnList>
FROM <tableNames>
[WHERE <condition>]
[ORDER BY <columnList>]
[GROUP BY <columnList>]
[HAVING]
```
