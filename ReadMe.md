# JOIN
A ```Join``` clause is used to combine rows from two or more tables, based on a related column between them.
Here are the main types of Joins:
* ```INNER JOIN```: Returns records that have matching values in both tables.
* ```LEFT JOIN```: Returns all records from the left table, and the matched records from the right table.
* ```RIGHT JOIN```: Returns all records from the right table, and the matched records from the left table.
* ```FULL JOIN```: Returns when there is a match in either left or right table.

Here are the procedures on how you can implement ```JOINS```
## SETUP
**Create Tables**: We will use two tables, `cars` and `customer` for our examples.
```sql
CREATE TABLE cars (
    car_id S
)
```

## Inner Join
An inner join returns records that have matching values in both tables. It only returns the rows where there's a match in both tables.

Example: Imagine we have two tables: Cars and Customers.

* Cars table:
* Customers table:

### Inner Join Query:
```sql
SELECT Cars.CarName, Customers.CustomerName
FROM Cars
INNER JOIN Customers
ON Cars.CustomerID = Customers.CustomerID;

```
Result:

## Left Join
A left join returns all records from the left table (Cars), and the matched records from the right table (Customers). The result is NULL from the right side if there is no match.

Example:

### Left Join Query:
```sql
SELECT Cars.CarName, Customers.CustomerName
FROM Cars
LEFT JOIN Customers
ON Cars.CustomerID = Customers.CustomerID;
```
Result:

## Right Join
A right join returns all records from the right table (Customers), and the matched records from the left table (Cars). The result is NULL from the left side when there is no match.

Example:

### Right Join Query:
```sql
SELECT Cars.CarName, Customers.CustomerName
FROM Cars
RIGHT JOIN Customers
ON Cars.CustomerID = Customers.CustomerID;
```
Result:

## Full Join
A full join returns all records when there is a match in either left or right table records. This means it returns all records from the left table (Cars) and the right table (Customers), with NULLs in places where the join condition is not met.

Example:

### Full Join Query:
```sql
SELECT Cars.CarName, Customers.CustomerName
FROM Cars
FULL OUTER JOIN Customers
ON Cars.CustomerID = Customers.CustomerID;
```
Result: