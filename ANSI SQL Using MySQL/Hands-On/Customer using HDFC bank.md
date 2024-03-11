# Customer using HDFC bank

Write a query to display the unique user name and their city who have booked their tickets by not using the HDFC bank for any of the bookings. Sort the result based on the user name.

(Note: Evaluate only the respective query to get the desired result. Data is case sensitive.

## Example

Assume there are few records in User & Booking Table

| User_id | name  | address   | Phoneno    | email           |
|---------|-------|-----------|------------|-----------------|
| 1001    | Adam  | Chennai   | 8988998991 | ada@gmail.com   |
| 1002    | Eve   | Mangalore | 1234567890 | eva@yahoo.com   |
| 1003    | John  | Mumbai    | 9087654321 | Jo@gmail.com    |
| 1004    | Peter | Hyderabad | 7867545343 | Peter@yahoo.co.in|

### BOOKING

| BD_ID | ACCNO    | NAME | USER_Id |
|-------|----------|------|---------|
| B1    | 12312324 | HDFC | 1001    |
| B2    | 23444434 | SBI  | 1001    |
| B3    | 54556444 | IOB  | 1002    |
| B4    | 45434234 | BOI  | 1003    |

### SAMPLE OUTPUT

| NAME | CITY      |
|------|-----------|
| EVE  | Mangalore |
| JOHN | Mumbai    |

Maintain the same sequence of column order as given in the problem description)

![Local Image](../images/BUSShema.JPG)

**Solution - **

`SELECT DISTINCT USERS.name, USERS.address FROM USERS 
JOIN BOOKINGDETAILS ON USERS.USER_ID = BOOKINGDETAILS.USER_ID
WHERE USERS.USER_ID NOT IN 
    (SELECT BOOKINGDETAILS.USER_ID FROM BOOKINGDETAILS
    WHERE BOOKINGDETAILS.NAME = "HDFC")
ORDER BY USERS.name;`