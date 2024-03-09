# Car Details Based on Type and Name

Write a query to display the car id, car name, and car type of Maruthi company 'Sedan' type cars. Sort the result based on car id.

(HINT: Use the `Cars` table to retrieve records. The car name is 'Maruthi Swift', and the car type is 'Sedan'. Data is case-sensitive.)

![Local Image](../images/Rental_car_mysql.png)

**NOTE:** Maintain the same sequence of column order, as specified in the question description.

**Solution - **

`sql
SELECT car_id, car_name, car_type 
FROM cars 
WHERE car_name LIKE 'Maruthi%' AND car_type='Sedan' 
ORDER BY car_id;`
