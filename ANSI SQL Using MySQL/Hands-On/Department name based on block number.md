# Department name based on block number

Write a query to display the names of the departments in block number 3. Sort the records in ascending order.

**NOTE:** Maintain the same sequence of column order, as specified in the question description.

![Local Image](../images/CMS_Mysql.JPG)

**Solution - **

`SELECT department_name FROM Department
WHERE department_block_number = 3
ORDER BY department_name;`