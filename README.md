# Llenguatge-SQL (Structured Query Language)

## WHAT is SQL?
- SQL stands for Structured Query Language. It's a language used to , users query, manipulate, and transform data stored in tables, a "relational database", collection of related (2D) tables, simular to Excel spreadsheets. Each table contains columns for the different fields, and rows for the different records. It provides a safe and scalable storage for websites and mobile applications.

## WHAT is a QUERY?
- A "query" is a statement which declares *what data* we are looking for, *where to find* it in the database, and *how to transform* it (before it is returned):

- TABLE(ENTITY):Dog 
- ROW (TYPE): puppie, huskie, labrador 
- COLUMN (PROPERTIES): Taillenght, Fur Color

## SQL statements structure
A "SQL statement" is composed of an ordered list of clauses and must always end with a semicolon (;).  
Each "clause" has its own syntax:
- SELECT
- FROM
- WHERE

## HOW TO RETRIEVE DATA FROM A SQL DATABASE? 
## 1. Write SELECT statement ("queries") to select data from a table:
#### SELECT all data in a table:
```
SELECT *
FROM employees;
```
#### SELECT specific columns
```
SELECT  name, age
FROM students;
```
#### SELECT without duplicated ROWS: 
The DISTINCT keyword will eliminate duplicated rows.
```
SELECT  DISTINCT name
FROM students;
```
Examples: 
- Select TITLE: ```SELECT Title FROM movies;```
- Select Director: ```SELECT Director FROM movies;```
- Select Title & Director: ```SELECT Title, Director FROM movies;``
- Select Title & Year: ```SELECT Title, Year FROM movies;```
- Select ALL: ```SELECT * FROM movies;```

## 2 ROWS
## 2.1 SORT rows 
The *ORDERED* keyword sort the rows:
```
SELECT name, age
FROM friends
ORDERED BY name, age DESC;
```
## 2.2 LIMIT rows 
```
SELECT name, grade
FROM course-grades
ORDERED BY grade DESC
LIMIT 5;
```
## 2.3 FILTER rows 
```
SELECT product
FROM inventory
WHERE code= 'ABCDE12345';
```

## 3 CONDITIONS 
### 3.1 CONDITIONS: numeric comparison
Columns and fields containing numeric values, can be used in conditions with *math comparison operators*:
```
- = (equals)
- < (less-than)
- <= (less-than or equals)
- > (greater-than)
- => (greater-than or equals)
- !=(does not equal)
```
```
SELECT product
FROM inventory
WHERE amount <= '10';
```
### 3.2 CONDITIONS: string comparison 
Columns and fields containing string values, can be used in conditions with *math comparison operators*:
```
- = (equals)
- < (before in dictionary order)
- <= (before or the same)
- > (after in dictionary order)
- => (After or the same)
- !=(does not equal)
- <>(does not equal)
```
```
SELECT product
FROM inventory
WHERE productName < 'B';
```
### 3.3 CONDITIONS: list possible values 
If a column can contain one or several possible values, filter a list with possible values with IN or NOT IN
```
SELECT product
FROM inventory
WHERE amount IN (1,5,19); 
```

### 3.4 CONDITIONS: inclusive ranges 
To match values WITHIN a given range, use the BETWEEN operator, for numbers, strings, dates and timestamps.
```
SELECT product
FROM inventory
WHERE amount BETWEEN 5 AND 9; // amount BETWEEN >=5 AND <=9; 
```
To match values OUTSIDE a given range, use the NOT BETWEEN operator, for numbers, strings, dates and timestamps.
```
SELECT product
FROM inventory
WHERE amount NOT BETWEEN 1 AND 4; // amount BETWEEN <1 AND >4; 
```

### 3.5 CONDITIONS: combining with AND 
To match valuesto 1+ conditions, in which ALL conditions have to match. 
```
SELECT product
FROM inventory
WHERE amount < 5 
AND price < 1;
```

### 3.6 CONDITIONS: combining with OR  
To match valuesto 1+ conditions, in which one or another condition has to match (NOT ALL). 
```
SELECT product
FROM inventory
WHERE amount < 5
OR price < 1;
```

### 3.7 CONDITIONS: mixing AND and OR  
To match values mixing condtions with both AND and OR operators, it is important to know that AND has a higher precedence and will be evaluated *BEFORE* OR.
```
SELECT product
FROM inventory
WHERE amount < 5 
OR name = 'paper'
AND price < 1;
```
If you want OR to be evaluated first, you need to use brackets () instead.
```
SELECT product
FROM inventory
WHERE (amount < 5
OR name = 'paper')
AND price < 1;
```
##SQL SYNTAX
####TABLE
```
- SELECT
- FROM
- WHERE 
- GROUP BY
- HAVING
- ORDER BY
```
####KEYWORDS
```
- DISTINCT
- LIMIT
- ASC
- DESC
```
####FILTERS & VALUES 
```
- <
- >
- =
- !=
- NOT
- IN
- BETWEEN
- AND
- OR
- (
- )
```

#### RESOURCES
- [SQLBOLT](https://sqlbolt.com/)
- [SQL](https://sqlpd.com/)
- [Exercisis SQL](https://josejuansanchez.org/bd/ejercicios-consultas-sql/index.html#ejercicios.-realizaci%C3%B3n-de-consultas-sql)
- [W3Schools-SQL](https://www.w3schools.com/sql/default.asp)

ENCARA NO HE ACABAT AQUET EXERCISI. 
- He fet 1.1.3 Consultas sobre una tabla fins a 36.
- Faltan: 
- 1.1.4 Consultas multitabla (Composición interna)
- 1.1.5 Consultas multitabla (Composición externa)
- 1.1.6 Consultas resumen
- 1.1.7 Subconsultas (En la cláusula WHERE)
