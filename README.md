# Llenguatge-SQL (Structured Query Language)

## WHAT is SQL?
- SQL is a "language" to allow users query, manipulate, and transform data from a "relational database", collection of related (2D) tables, simular to Excel spreadsheets, with a fixed number of columns (table attributes or properties) and any number of rows of data.
- SQL provides a safe and scalable storage for websites and mobile applications.

## WHAT is a QUERY?
- A "query" is a statement which declares:
1) what data we are looking for, 
2) where to find it in the database, 
3) and how to transform it (before it is returned).


in SQL 
- a TABLE: Dog (ENTITY)
- ROW: puppie, huskie, labrador (SPECIFIC INSTANCE OF TYPE)
- COLUMN: Taillenght, Fur Color (COMMON PROPERTIES)


## HOW TO RETRIEVE DATA FROM A SQL DATABASE? 
-  write SELECT statements ("queries"):

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
Select TITLE: ```SELECT Title FROM movies;```
Select Director: ```SELECT Director FROM movies;```
Select Title & Director: ```SELECT Title, Director FROM movies;``
Select Title & Year: ```SELECT Title, Year FROM movies;```
Select ALL: ```SELECT * FROM movies;```



- [SQLBOLT](https://sqlbolt.com/)
- [Exercisis SQL](https://josejuansanchez.org/bd/ejercicios-consultas-sql/index.html#ejercicios.-realizaci%C3%B3n-de-consultas-sql)
- [W3Schools-SQL](https://www.w3schools.com/sql/default.asp)

Encara no he començat aquet exercisi


