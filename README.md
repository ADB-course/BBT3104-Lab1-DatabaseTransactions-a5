[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/r-tQZu0l)
# BBT3104-Lab1of6-DatabaseTransactions


| **Key**                                                               | Value                                                                                                                                                                              |
|---------------|---------------------------------------------------------|
| **Group Name**                                                               | ? |
| **Semester Duration**                                                 | 19<sup>th</sup> August - 25<sup>th</sup> November 2024                                                                                                                       |

## Flowchart
[Start]
    |
    v
[Create Order]
    |
    v
[Insert Order Details] --> [Update Stock Quantity]
    |
    v
[Receive Payment]
    |
    v
[Insert Payment Details]
    |
    v
[Error Check]
    |
    v
  /   \
 /     \
v       v
[Rollback] [Commit]
    |        |
    v        v
[End]     [End]

## Pseudocode
BEGIN TRANSACTION
  Create order:
    Insert order details into orderdetails table.
    Update quantity in stock in products table.

  Receive payment:
    Insert payment details into payments table.

  IF ERROR OCCURS THEN
    ROLLBACK TRANSACTION
  ELSE
    COMMIT TRANSACTION
END TRANSACTION
## Support for the Sales Departments' Report
BEGIN TRANSACTION
 1.Create order and update quantity in stock
    INSERT INTO orderdetails (OrderNumber, productcode, quantityOrdered, priceEach, orderLineNumber)
    VALUE(@OrderNumber, 1518_17491, 2724,'136', 1)

    UPDATE 'products' SET 'quantityinSTOCK
    =@quantityinstock-2724 WHERE 'productcode' ='518_1749

2. Receive payment for order made
   INSERT INTO payments
    (CustomerNumber, checkNumber, paymentDate, amount)

   IF ERROR OCCURS THEN
       ROLLBACK TRANSACTION
   ELSE
     COMMIT TRANSACTION

END TRANSACTION