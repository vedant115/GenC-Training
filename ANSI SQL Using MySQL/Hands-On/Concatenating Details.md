# Concatenating Details

Write a query to display address details by concatenating address and city of students. Give an alias as Address and sort the result based on the concatenated column in descending order.

**Example**: 

           Address - Toms Town

           City - Bangalore

**Output**:

           Toms Town, Bangalore

**NOTE**: Maintain the same sequence of column order, as specified in the question description

![Local Image](../images/CMS_Mysql.JPG)

**Solution - **

`SELECT CONCAT(address, ", ", city) as Address FROM Student ORDER BY Address DESC;`