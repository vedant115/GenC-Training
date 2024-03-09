# Customers Having Gmail ID

Write a query to display the customer id, customer name, address, and phone number of customers having a Gmail id. Sort the result based on customer id.

(HINT: Use the `Customers` table to retrieve records. The email id format is 'xxxxx@gmail.com'. Data is case-sensitive.)

**NOTE:** Maintain the same sequence of column order, as specified in the question description.

![Local Image](../images/Rental_car_mysql.png)

**Solution - **

`UPDATE customersSET phone_no = 9876543210WHERE customer_id = "CUST1004";`
