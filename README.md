# Llenguatge-SQL (Structured Query Language)

## WHAT is SQL?
- SQL is a "language" to allow users query, manipulate, and transform data from a "relational database", collection of related (2D) tables, simular to Excel spreadsheets, with a fixed number of columns (table attributes or properties) and any number of rows of data.
- SQL provides a safe and scalable storage for websites and mobile applications.

## WHAT is a QUERY?
- A "query" is a statement which declares:
1) what data we are looking for, 
2) where to find it in the database, 
3) and how to transform it (before it is returned).

- TABLE (ENTITY):Dog
- ROW (SPECIFIC INSTANCE OF TYPE): puppie, huskie, labrador
- COLUMN (COMMON PROPERTIES): Taillenght, Fur Color

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

### 2 QUERIES WITH CONSTRAINTS (WHERE)
= to filter certain results from being returned.
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
Operator	                 Condition	                               SQL Example
=, !=, < <=, >, >=	       Standard numerical operators	            col_name != 4
BETWEEN … AND …	          Number within two values (inclusive)	    col_name BETWEEN 1.5 AND 10.5
NOT BETWEEN … AND        	Number NOT within two values (inclusive)	col_name NOT BETWEEN 1 AND 10
IN (…)	                   Number exists in a list	                 col_name IN (2, 4, 6)
NOT IN (…)	               Number does not exist in a list	         col_name NOT IN (1, 3, 5)
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

```

```


### 3 QUERIES WITH CONSTRAINTS

### 4 QUERIES WITH CONSTRAINTS

### 5 QUERIES WITH CONSTRAINTS

### 6 QUERIES WITH CONSTRAINTS

### 7 QUERIES WITH CONSTRAINTS

### 8 QUERIES WITH CONSTRAINTS

### 9 QUERIES WITH CONSTRAINTS

### 10 QUERIES WITH CONSTRAINTS

### 11 QUERIES WITH CONSTRAINTS

### 12 QUERIES WITH CONSTRAINTS

- [SQLBOLT](https://sqlbolt.com/)
- [Exercisis SQL](https://josejuansanchez.org/bd/ejercicios-consultas-sql/index.html#ejercicios.-realizaci%C3%B3n-de-consultas-sql)
- [W3Schools-SQL](https://www.w3schools.com/sql/default.asp)

Encara no he començat aquet exercisi


