# SQL Lesson 11: Queries with aggregates (Pt. 2)

Our queries are getting fairly complex, but we have nearly introduced all the important parts of a `SELECT` query. One thing that you might have noticed is that if the `GROUP BY` clause is executed after the `WHERE` clause (which filters the rows which are to be grouped), then how exactly do we filter the grouped rows?

Luckily, SQL allows us to do this by adding an additional `HAVING` clause which is used specifically with the `GROUP BY` clause to allow us to filter grouped rows from the result set.

Select query with HAVING constraint

```sql
SELECT group_by_column, AGG_FUNC(column_expression) AS aggregate_result_alias, … 
FROM mytable 
WHERE condition 
GROUP BY column HAVING group_condition;
```

==简单来说HAVING函数就是用来给GROUP BY 函数进行一个限定的==



```sql
--SELECT * FROM employees;
-- Q1
SELECT COUNT(Role) AS NUM_ARTISTS
FROM Employees
WHERE Role = "Artist";

-- Q2
SELECT Role, COUNT(Role) AS NUM_ARTISTS
FROM Employees
GROUP BY Role;

-- Q3
SELECT Role, SUM(Years_employed) AS SUM_EMPLOYED
FROM Employees
GROUP BY Role
HAVING Role = "Engineer";

```

![image-20250426215830625](11_Queries_with_aggregates(Pt.2).assets/image-20250426215830625.png)