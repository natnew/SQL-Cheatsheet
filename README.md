# SQL-Cheatsheet
SQL Cheatsheet

![A python cheatsheet](https://github.com/natnew/Python-Cheatsheet/blob/main/Python%20Cheatsheet.JPG)

## Contents 
**[`Introduction`](#Introduction)** <br>
**[`Comments`](#Comments)** <br>
**[`Commands`](#Commands)** <br>
**[`Operators`](#Operators)** <br>
**[`Logical`](#Logical)** <br>

## Introduction

## Comments
```sql
-- Select all:
```

## Commands
```sql
SELECT
```
```sql
UPDATE
```
```sql
DELETE
```
```sql
INSERT INTO
```
```sql
CREATE DATABASE
```
```sql
ALTER DATABASE
```
```sql
CREATE TABLE
```
```sql
ALTER TABLE
```
```sql
DROP TABLE
```
```sql
CREATE INDEX
```
```sql
DROP INDEX
```

## Operators
```sql
SELECT 30 + 20;
```
```sql
SELECT 30 - 20;
```
```sql
SELECT 30 * 20;
```
```sql
SELECT 30 / 20;
```
```sql
SELECT 30 % 20;
```

## Comparison
```sql
SELECT * FROM Products
WHERE Price = 18;
```
```sql
SELECT * FROM Products
WHERE Price > 18;
```
```sql
SELECT * FROM Products
WHERE Price < 18;
```
```sql
SELECT * FROM Products
WHERE Price >= 18;
```
```sql
SELECT * FROM Products
WHERE Price <= 18;
```
```sql
SELECT * FROM Products
WHERE Price <> 18;
```

## Logical
```sql
SELECT ProductName 
FROM Products
WHERE ProductID = ALL (SELECT ProductID FROM OrderDetails WHERE Quantity = 10);

```
```sql
SELECT * FROM Customers
WHERE City = "London" AND Country = "UK";

```
```sql
SELECT * FROM Products
WHERE Price > ANY (SELECT Price FROM Products WHERE Price > 50);

```
```sql
SELECT * FROM Products
WHERE Price BETWEEN 50 AND 60;

```
```sql
SELECT SupplierName
FROM Suppliers
WHERE EXISTS (SELECT ProductName FROM Products WHERE Products.SupplierID = Suppliers.supplierID AND Price < 20);


```
```sql
SELECT SupplierName
FROM Suppliers
WHERE EXISTS (SELECT ProductName FROM Products WHERE Products.SupplierID = Suppliers.supplierID AND Price < 20);

```
```sql
SELECT * FROM Customers
WHERE City IN ('Paris','London');


```
```sql
SELECT * FROM Customers
WHERE City LIKE 's%';


```
```sql
SELECT ProductName 
FROM Products
WHERE ProductID = ALL (SELECT ProductID FROM OrderDetails WHERE Quantity = 10);

```
```sql
SELECT * FROM Customers
WHERE City NOT LIKE 's%';

```
```sql
SELECT * FROM Customers
WHERE City = "London" OR Country = "UK";

```
```sql
SELECT * FROM Products
WHERE Price > SOME (SELECT Price FROM Products WHERE Price > 20);

```
