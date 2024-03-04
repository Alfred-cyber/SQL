# SQL
SQL Commands That can Simplify Your Work
# Check out some of the basics
-- Create a new table
CREATE TABLE employees (
    employee_id INT PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    salary DECIMAL(10, 2)
);

-- Insert data into the table
INSERT INTO employees (employee_id, first_name, last_name, salary)
VALUES (1, 'John', 'Doe', 50000),
       (2, 'Jane', 'Smith', 60000),
       (3, 'Bob', 'Johnson', 75000);

-- Update a record in the table
UPDATE employees
SET salary = 80000
WHERE employee_id = 1;

-- Select data from the table
SELECT * FROM employees;

-- Create an index on the 'last_name' column
CREATE INDEX idx_last_name
ON employees (last_name);

-- Delete a record from the table
DELETE FROM employees
WHERE employee_id = 2;

-- Revoke a privilege
REVOKE SELECT
ON employees FROM user_name;
