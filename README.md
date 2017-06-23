# Database-SQL

## Find N th highest salary in SQL. 

How to find max salary in SQL 

Using sub-query.  
   First highest salary 
   SELECT MAX(Salary) 
   FROM Employees; 

* Second highest salary
   SELECT MAX(Salary) 
   FROM Employees 
   WHERE Salary < (SELECT MAX(Salary) FROM Employees); 

* N th highest salary using a sub-query. 
   SELECT DISTINCT TOP 2 Salary
   FROM Employees
   ORDER BY Salary DESC;

   SELECT TOP 1 Salary from 
   (SELECT DISTINCT TOP 2 Salary
   FROM Employees
   ORDER BY Salary DESC) Result
   ORDER BY Salary; 
   

   
