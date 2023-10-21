**SQL Table Creation and Data Insertion:**

```sql
-- Create the Employee table
CREATE TABLE Employee (
    EmployeeID INT PRIMARY KEY,
    FirstName VARCHAR(50),
    LastName VARCHAR(50),
    Department VARCHAR(50),
    Salary DECIMAL(10, 2)
);

-- Insert 20 sample records into the Employee table
INSERT INTO Employee (EmployeeID, FirstName, LastName, Department, Salary)
VALUES
    (1, 'John', 'Doe', 'HR', 50000.00),
    (2, 'Jane', 'Smith', 'IT', 60000.00),
    (3, 'Michael', 'Johnson', 'Finance', 55000.00),
    (4, 'Emily', 'Brown', 'Marketing', 52000.00),
    (5, 'David', 'Wilson', 'Sales', 55000.00),
    (6, 'Sarah', 'Lee', 'IT', 62000.00),
    (7, 'James', 'Anderson', 'Finance', 58000.00),
    (8, 'Olivia', 'Martinez', 'HR', 52000.00),
    (9, 'Daniel', 'Taylor', 'Sales', 56000.00),
    (10, 'Sophia', 'Jackson', 'Marketing', 53000.00),
    (11, 'Liam', 'Harris', 'IT', 61000.00),
    (12, 'Ava', 'White', 'Finance', 57000.00),
    (13, 'William', 'Miller', 'HR', 51000.00),
    (14, 'Ella', 'Thompson', 'Marketing', 54000.00),
    (15, 'Alexander', 'Walker', 'Sales', 57000.00),
    (16, 'Mia', 'Clark', 'IT', 59000.00),
    (17, 'Henry', 'Lewis', 'Finance', 59000.00),
    (18, 'Sofia', 'Hall', 'HR', 53000.00),
    (19, 'Jackson', 'Young', 'Sales', 58000.00),
    (20, 'Luna', 'Wright', 'Marketing', 55000.00);
```

**General Questions:**
1. What is the structure of the Employee table?
2. How many columns are there in the Employee table?
3. What is the primary key of the Employee table?
4. Can you retrieve all the records from the Employee table?
5. How many records (rows) are there in the Employee table?

**Data Retrieval:**
6. Show me the first 5 records from the Employee table.
7. Display the names of all employees in the Marketing department.
8. Retrieve the highest salary in the Employee table.
9. List the employees whose salary is above $55,000.
10. Who has the lowest salary in the IT department?
11. Find the employee with EmployeeID 7.

**Data Modification:**
12. Update the salary of John Doe to $52,000.
13. Insert a new employee with EmployeeID 21, FirstName 'Isabella,' LastName 'Davis,' Department 'Sales,' and Salary $57,000.
14. Delete the record of employee with EmployeeID 9.
15. Change the department of employee with EmployeeID 14 to 'Finance.'

**Aggregation and Statistics:**
16. Calculate the average salary of all employees.
17. What is the total salary expenditure for the company?
18. Find the department with the highest average salary.
19. Count the number of employees in each department.
20. What is the sum of salaries for employees in the IT department?

**Sorting and Filtering:**
21. List employees in ascending order of their salaries.
22. Show the top 3 highest-paid employees.
23. Display employees with a salary between $50,000 and $60,000.
24. Sort employees by their last names in alphabetical order.
25. Find employees with names starting with 'A.'

**Grouping and Aggregation:**
26. Group employees by department and show the total count in each department.
27. Calculate the average salary for each department.
28. What is the highest salary in the Sales department?
29. List departments with more than 3 employees.
30. Find the department with the most employees.

**Joins and Relationships:**
31. Do you have any information about the managers of each department?
32. Show employees who do not belong to any department.
33. List employees along with their department names.
34. Retrieve employees who have the same last name.
35. Find employees with the same department and salary.

**Advanced Queries:**
36. Find the employee(s) with the second-highest salary.
37. Display the employee(s) with the longest first name.
38. Calculate the salary difference between employees with EmployeeID 3 and 6.
39. List employees who earn more than the average salary in their department.
40. Show the employees with the highest salary within each department.



**General Questions:**

1. What is the structure of the Employee table?
The structure of the "Employee" table is as follows:

EmployeeID (INT, PRIMARY KEY): This column stores the unique identifier for each employee.
FirstName (VARCHAR(50)): This column stores the first name of the employee.
LastName (VARCHAR(50)): This column stores the last name of the employee.
Department (VARCHAR(50)): This column stores the department in which the employee works.
Salary (DECIMAL(10, 2)): This column stores the salary of the employee as a decimal number with 10 total digits and 2 decimal places.

2. How many columns are there in the Employee table?
There are five columns in the "Employee" table.

3. What is the primary key of the Employee table?
The primary key of the "Employee" table is the "EmployeeID" column.

4. Can you retrieve all the records from the Employee table?
To retrieve all the records from the "Employee" table, you can use the following SQL query:
SELECT * FROM Employee;

5. How many records (rows) are there in the Employee table?
There are 20 records (rows) in the "Employee" table

**Data Retrieval:**
6. Show me the first 5 records from the Employee table.
SELECT * FROM Employee
LIMIT 5;

7. Display the names of all employees in the Marketing department.
SELECT FirstName, LastName
FROM Employee
WHERE Department = 'Marketing';

8. Retrieve the highest salary in the Employee table.
SELECT MAX(Salary) AS HighestSalary
FROM Employee;

9. List the employees whose salary is above $55,000.
SELECT FirstName, LastName
FROM Employee
WHERE Salary > 55000.00;

10. Who has the lowest salary in the IT department?
SELECT FirstName, LastName
FROM Employee
WHERE Department = 'IT'
ORDER BY Salary ASC
LIMIT 1;

11. Find the employee with EmployeeID 7.
SELECT * FROM Employee
WHERE EmployeeID = 7;


**Data Modification:**
12. Update the salary of John Doe to $52,000.
UPDATE Employee
SET Salary = 52000.00
WHERE EmployeeID = 1;

13. Insert a new employee with EmployeeID 21, FirstName 'Isabella,' LastName 'Davis,' Department 'Sales,' and Salary $57,000.
INSERT INTO Employee (EmployeeID, FirstName, LastName, Department, Salary)
VALUES (21, 'Isabella', 'Davis', 'Sales', 57000.00);

14. Delete the record of employee with EmployeeID 9.
DELETE FROM Employee
WHERE EmployeeID = 9;

15. Change the department of employee with EmployeeID 14 to 'Finance.'
UPDATE Employee
SET Department = 'Finance'
WHERE EmployeeID = 14;

**Aggregation and Statistics:**

16. Calculate the average salary of all employees.
SELECT AVG(Salary) AS AverageSalary
FROM Employee;

17. What is the total salary expenditure for the company?
SELECT SUM(Salary) AS TotalSalaryExpenditure
FROM Employee;

18. Find the department with the highest average salary.
SELECT Department, AVG(Salary) AS AverageSalary
FROM Employee
GROUP BY Department
ORDER BY AverageSalary DESC
LIMIT 1;

19. Count the number of employees in each department.
SELECT Department, COUNT(*) AS EmployeeCount
FROM Employee
GROUP BY Department;

20. What is the sum of salaries for employees in the IT department?
SELECT SUM(Salary) AS TotalSalaryExpenditureIT
FROM Employee
WHERE Department = 'IT';

**Sorting and Filtering:**

21. List employees in ascending order of their salaries.
SELECT * FROM Employee
ORDER BY Salary ASC;

22. Show the top 3 highest-paid employees.
SELECT * FROM Employee
ORDER BY Salary DESC
LIMIT 3;

23. Display employees with a salary between $50,000 and $60,000.
SELECT * FROM Employee
WHERE Salary BETWEEN 50000.00 AND 60000.00;

24. Sort employees by their last names in alphabetical order.
SELECT * FROM Employee
ORDER BY LastName ASC;

25. Find employees with names starting with 'A.'
SELECT * FROM Employee
WHERE FirstName LIKE 'A%';


**Grouping and Aggregation:**
26. Group employees by department and show the total count in each department.
SELECT Department, COUNT(*) AS EmployeeCount
FROM Employee
GROUP BY Department;

27. Calculate the average salary for each department.
SELECT Department, AVG(Salary) AS AverageSalary
FROM Employee
GROUP BY Department;

28. What is the highest salary in the Sales department?
SELECT MAX(Salary) AS HighestSalaryInSales
FROM Employee
WHERE Department = 'Sales';

29. List departments with more than 3 employees.
SELECT Department
FROM Employee
GROUP BY Department
HAVING COUNT(*) > 3;

30. Find the department with the most employees.
SELECT Department, COUNT(*) AS EmployeeCount
FROM Employee
GROUP BY Department
ORDER BY EmployeeCount DESC
LIMIT 1;

**Joins and Relationships:**

31. Do you have any information about the managers of each department?

32. Show employees who do not belong to any department.
SELECT * FROM Employee
WHERE Department IS NULL;

33. List employees along with their department names.
SELECT FirstName, LastName, Department
FROM Employee;

34. Retrieve employees who have the same last name.
SELECT LastName, COUNT(*) AS NameCount
FROM Employee
GROUP BY LastName
HAVING COUNT(*) > 1;

35. Find employees with the same department and salary.
SELECT Department, Salary, COUNT(*) AS EmployeeCount
FROM Employee
GROUP BY Department, Salary
HAVING COUNT(*) > 1;


**Advanced Queries:**

36. Find the employee(s) with the second-highest salary.
SELECT * FROM Employee
WHERE Salary = (
    SELECT DISTINCT Salary
    FROM Employee
    ORDER BY Salary DESC
    LIMIT 1 OFFSET 1
);

37. Display the employee(s) with the longest first name.
SELECT * FROM Employee
WHERE LENGTH(FirstName) = (
    SELECT MAX(LENGTH(FirstName))
    FROM Employee
);

38. Calculate the salary difference between employees with EmployeeID 3 and 6.
SELECT (SELECT Salary FROM Employee WHERE EmployeeID = 6) - (SELECT Salary FROM Employee WHERE EmployeeID = 3) AS SalaryDifference;

39. List employees who earn more than the average salary in their department.
SELECT e.*
FROM Employee e
INNER JOIN (
    SELECT Department, AVG(Salary) AS AvgSalary
    FROM Employee
    GROUP BY Department
) AS dept_avg ON e.Department = dept_avg.Department
WHERE e.Salary > dept_avg.AvgSalary;

40. Show the employees with the highest salary within each department.
SELECT e.*
FROM Employee e
INNER JOIN (
    SELECT Department, MAX(Salary) AS MaxSalary
    FROM Employee
    GROUP BY Department
) AS dept_max ON e.Department = dept_max.Department AND e.Salary = dept_max.MaxSalary;


