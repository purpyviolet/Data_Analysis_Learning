# **SQL Lesson 10: Queries with aggregates (Pt. 1)**

In addition to the simple expressions that we introduced last lesson, SQL also supports the use of aggregate expressions (or functions) that allow you to summarize information about a group of rows of data. With the Pixar database that you've been using, aggregate functions can be used to answer questions like, "How many movies has Pixar produced?", or "What is the highest grossing Pixar film each year?".

Select query with aggregate functions over all rows

```sql
SELECT AGG_FUNC(column_or_expression) AS aggregate_description, … 
FROM mytable 
WHERE constraint_expression;
```

# Common aggregate functions

Here are some common aggregate functions that we are going to use in our examples:

| Function                              | Description                                                  |
| ------------------------------------- | ------------------------------------------------------------ |
| **COUNT(*****)**, **COUNT(*column*)** | A common function used to counts the number of rows in the group if no column name is specified. Otherwise, count the number of rows in the group with non-NULL values in the specified column. |
| **MIN(*column*)**                     | Finds the smallest numerical value in the specified column for all rows in the group. |
| **MAX(*column*)**                     | Finds the largest numerical value in the specified column for all rows in the group. |
| **AVG(*column*)**                     | Finds the average numerical value in the specified column for all rows in the group. |
| **SUM(*column*)**                     | Finds the sum of all numerical values in the specified column for the rows in the group. |

# Grouped aggregate functions

In addition to aggregating across all the rows, you can instead apply the aggregate functions to individual groups of data within that group (ie. box office sales for Comedies vs Action movies).
This would then create as many results as there are unique groups defined as by the `GROUP BY` clause.

Select query with aggregate functions over groups

```sql
SELECT AGG_FUNC(column_or_expression) AS aggregate_description, … 
FROM mytable 
WHERE constraint_expression 
GROUP BY column;
```

==**GROUP BY 函数轻松实现对于column中单独属性的统计**==

```sql
--SELECT * FROM employees;
-- Q1
SELECT Role, Name, MAX(Years_employed) AS LONGEST_EMPLOYEE
FROM Employees;
-- Q2
SELECT Role, AVG(Years_employed) AS AVG_EMPLOYEED
FROM Employees
GROUP BY Role;
-- Q3
SELECT Building, SUM(Years_employed) AS TOTAL_EMPLOYEED
FROM Employees
GROUP BY Building;
```

![image-20250426214219211](10_Queries_with_aggregates(Pt.1).assets/image-20250426214219211.png)