# Employees-from-database
use employees;
SELECT 
    dm.*, d.*
FROM
    dept_manager dm
        CROSS JOIN
    departments d ON dm.dept_no = d.dept_no
WHERE
    d.dept_no = 'd009';
    
    
/* SELECT 
    de.emp_no, e.first_name, e.last_name, d.dept_no, d.dept_name
FROM
    employees e
        CROSS JOIN
    departments d
        JOIN
    dept_emp de ON d.dept_no = de.dept_no
LIMIT 10; */

SELECT e.*, d.* FROM employees e CROSS JOIN departments d WHERE e.emp_no < 10011 ORDER BY e.emp_no, d.dept_name;
