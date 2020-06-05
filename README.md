# Llenguatge-SQL (Structured Query Language)

## WHAT is SQL?
- SQL stands for Structured Query Language. It's a language used to , users query, manipulate, and transform data stored in tables, a "relational database", collection of related (2D) tables, simular to Excel spreadsheets. Each table contains columns for the different fields, and rows for the different records. It provides a safe and scalable storage for websites and mobile applications.

## WHAT is a QUERY?
- A "query" is a statement which declares:
1) what data we are looking for, 
2) where to find it in the database, 
3) and how to transform it (before it is returned).

- TABLE (ENTITY):Dog
- ROW (SPECIFIC INSTANCE OF TYPE): puppie, huskie, labrador
- COLUMN (COMMON PROPERTIES): Taillenght, Fur Color

## Structure of an SQL state
A SQL statement is composed of an ordered list of clauses such as: 
- SELECT
- FROM
- WHERE
Each clause has its own syntax.
- An SQL statement must always end with a semicolon (;).

## SQL statements
1 #### SELECT statement
SELECT all data in a table
```
SELECT *
FROM employees;
```
1 #### SELECT statement


## HOW TO RETRIEVE DATA FROM A SQL DATABASE? 
-  write SELECT statements ("queries"):

### 1 SELECT QUERIES (SELECT)= select for specific columns of data from a table:
 
Select query for specific columns
```
Select query for a specific columns
SELECT column, another_column, …
FROM mytable;
```
Select query for ALL columns
```
Select query for all columns
SELECT * 
FROM mytable;
```
Examples: 
- Select TITLE: ```SELECT Title FROM movies;```
- Select Director: ```SELECT Director FROM movies;```
- Select Title & Director: ```SELECT Title, Director FROM movies;``
- Select Title & Year: ```SELECT Title, Year FROM movies;```
- Select ALL: ```SELECT * FROM movies;```


### 2 QUERIES WITH CONSTRAINTS (WHERE)= to filter certain results from being returned.
"WHERE" is applied to each row of data by checking specific column values to determine if it should be included in the results or not.
```
Select query with constraints
SELECT column, another_column, …
FROM mytable
WHERE condition
    AND/OR another_condition
    AND/OR …;
 ```
```
Operator	                  Condition	                                  SQL Example
=, !=, < <=, >, >=	          Standard numerical operators	              col_name != 4
BETWEEN … AND …	             Number within two values (inclusive)	      col_name BETWEEN 1.5 AND 10.5
NOT BETWEEN … AND        	   Number NOT within two values (inclusive)  	col_name NOT BETWEEN 1 AND 10
IN (…)	                      Number exists in a list	                   col_name IN (2, 4, 6)
NOT IN (…)	                  Number does not exist in a list	           col_name NOT IN (1, 3, 5)
```

Examples: 
- Find the movie with a row id of 6: 
```
SELECT id, title FROM movies 
   WHERE id = 6;
```
- Find the movies released in the years between 2000 and 2010:
```
SELECT title, year FROM movies
   WHERE year BETWEEN 2000 AND 2010;
```
- Find the movies not released in the years between 2000 and 2010
```
SELECT title, year FROM movies
WHERE year NOT BETWEEN 2000 AND 2010;
```
- Find the first 5 Pixar movies and their release year
```
SELECT title, year FROM movies
WHERE year <= 2003;
```


### 3 QUERIES WITH CONSTRAINTS-2
```
Operator	Condition	Example
=	Case sensitive exact string comparison (notice the single equals)	col_name = "abc"
!= or <>	Case sensitive exact string inequality comparison	col_name != "abcd"
LIKE	Case insensitive exact string comparison	col_name LIKE "ABC"
NOT LIKE	Case insensitive exact string inequality comparison	col_name NOT LIKE "ABCD"
%	Used anywhere in a string to match a sequence of zero or more characters (only with LIKE or NOT LIKE)	col_name LIKE "%AT%"
(matches "AT", "ATTIC", "CAT" or even "BATS")
_	Used anywhere in a string to match a single character (only with LIKE or NOT LIKE)	col_name LIKE "AN_"
(matches "AND", but not "AN")
IN (…)	String exists in a list	col_name IN ("A", "B", "C")
NOT IN (…)	String does not exist in a list	col_name NOT IN ("D", "E", "F")
```

Examples: 
- Find all the Toy Story movies: 
```
SELECT title, director FROM movies 
WHERE title LIKE "Toy Story%";
```
- Find all the movies directed by John Lasseter:
```
SELECT title, director FROM movies 
WHERE director LIKE "John Lasseter";
```
- Find all the movies (and director) not directed by John Lasseter
```
SELECT title, director FROM movies 
WHERE director != "John Lasseter";
```
- Find all the WALL-* movies
```
SELECT * FROM movies 
WHERE title LIKE "WALL-_";
```

### 4 QUERIES Filtering and sorting Query results
### 5 QUERIES Simple SELECT Queries
### 6 Multi-table queries with JOINs
### 7 OUTER JOINs
### 8 A short note on NULLs

### 9 Queries with expressions
### 10 Queries with aggregates 

### 11 Order of execution of a Query

### 12 Inserting rows
### 13  Updating rows
### 14 Deleting rows

### 15 Creating tables
### 16 Altering tables
### 17 Dropping tables

#### RESOURCES
- [SQLBOLT](https://sqlbolt.com/)
- [Exercisis SQL](https://josejuansanchez.org/bd/ejercicios-consultas-sql/index.html#ejercicios.-realizaci%C3%B3n-de-consultas-sql)
- [W3Schools-SQL](https://www.w3schools.com/sql/default.asp)

Encara no he començat aquet exercisi


