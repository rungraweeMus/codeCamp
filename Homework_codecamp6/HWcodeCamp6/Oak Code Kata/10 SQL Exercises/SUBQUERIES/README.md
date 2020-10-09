# SQL Exercises
## SUBQUERIES
1. Write a query to display all the orders from the orders table issued by the salesman 'Paul Adam'.  

    ![Imgur](https://i.imgur.com/KWGQj4l.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT *
        FROM orders
        WHERE salesman_id =
            (SELECT salesman_id 
            FROM salesman 
            WHERE name='Paul Adam');
    
    |ord_no	|purch_amt	|ord_date	|customer_id	|salesman_id|
    |---|---|---|---|---|
    |70011	|75.29		|2012-08-17	|3003		|5007|

___
2. Write a query to display all the orders for the salesman who belongs to the city London.  

    ![Imgur](https://i.imgur.com/KWGQj4l.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT *
        FROM orders
        WHERE salesman_id =
            (SELECT salesman_id 
            FROM salesman 
            WHERE city='London');
    
    |ord_no	|purch_amt	|ord_date	|customer_id	|salesman_id
    |---|---|---|---|---|
    |70009	|270.65		|2012-09-10	|3001		|5005|

___
3. Write a query to find all the orders issued against the salesman who may works for customer whose id is 3007.  

    ![Imgur](https://i.imgur.com/KWGQj4l.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

    SELECT *
    FROM orders
    WHERE salesman_id =
        (SELECT DISTINCT salesman_id 
        FROM orders 
        WHERE customer_id =3007);
    
    |ord_no	|purch_amt	|ord_date	|customer_id	|salesman_id|
    |---|---|---|---|---|---|---|
    |70002	|65.26		|2012-10-05	|3002		|5001|
    |70005	|2400.60		|2012-07-27	|3007		|5001|
    |70008	|5760.00		|2012-09-10	|3002		|5001|
    |70013	|3045.60		|2012-04-25	|3002		|5001|

___
4. Write a query to display all the orders which values are greater than the average order value for 10th October 2012.  

    ![Imgur](https://i.imgur.com/KWGQj4l.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT *
        FROM orders
        WHERE purch_amt >
            (SELECT  AVG(purch_amt) 
            FROM orders 
            WHERE ord_date ='10/10/2012');
    
    |ord_no	|purch_amt	|ord_date	|customer_id	|salesman_id|
    |---|---|---|---|---|---|
    |70005	|2400.60		|2012-07-27	|3007		|5001|
    |70008	|5760.00		|2012-09-10	|3002		|5001|
    |70003	|2480.40		|2012-10-10	|3009		|5003|
    |70013	|3045.60		|2012-04-25	|3002		|5001|

___
5. Write a query to find all orders attributed to a salesman in New york.  

    ![Imgur](https://i.imgur.com/KWGQj4l.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT *
        FROM orders
        WHERE salesman_id IN
            (SELECT salesman_id 
            FROM salesman 
            WHERE city ='New York');
    
    |ord_no	|purch_amt	|ord_date	|customer_id	|salesman_id|
    |---|---|---|---|---|
    |70002	|65.26		|2012-10-05	|3002		|5001|
    |70005	|2400.60		|2012-07-27	|3007		|5001|
    |70008	|5760.00		|2012-09-10	|3002		|5001|
    |70013	|3045.60		|2012-04-25	|3002		|5001|

___
6. Write a query to display the commission of all the salesmen servicing customers in Paris.  

    ![Imgur](https://i.imgur.com/cd0UQ1R.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT commission
        FROM salesman
        WHERE salesman_id IN
            (SELECT salesman_id 
            FROM customer
            WHERE city = 'Paris');


    |commission|
    |---|
    |0.14|

___

7. Write a query to display all the customers whose id is 2001 bellow the salesman ID of Mc Lyon.  

    ![Imgur](https://i.imgur.com/cd0UQ1R.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT *
        FROM customer
        WHERE customer_id =
            (SELECT salesman_id -2001
            FROM salesman
            WHERE name = 'Mc Lyon');
   
    |customer_id	|cust_name	|city		|grade	|salesman_id|
    |---|---|---|---|---|---|---|
    |3005		|Graham Zusi	|California	|200		|5002|

___
 
8. Write a query to count the customers with grades above New York's average.  

    ![Imgur](https://i.imgur.com/xNTaFOq.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

    SELECT grade, COUNT (*)
    FROM customer
    GROUP BY grade
    HAVING grade >
        (SELECT AVG(grade)
        FROM customer
        WHERE city = 'New York');
    
    |grade	|count|
    |---|---|
    |200		|3|
    |300		|2|
___
9. Write a query to extract the data from the orders table for those salesman who earned the maximum commission  

    ![Imgur](https://i.imgur.com/5josRY9.png)
    ![Imgur](https://i.imgur.com/6AtwDjj.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT ord_no, purch_amt, ord_date, salesman_id 
        FROM orders 
        WHERE salesman_id IN(
            SELECT salesman_id 
            FROM salesman
            WHERE commission = (
            SELECT MAX(commission) 
            FROM salesman));
    
   | ord_no | purch_amt |  ord_date  | salesman_id |
   | ----|-----|-----|------|
   | 70002 |     65.26 | 2012-10-05 |        5001|
   | 70005 |   2400.60 | 2012-07-27 |        5001|
   | 70008 |   5760.00 | 2012-09-10 |        5001|
   | 70013 |   3045.60 | 2012-04-25 |        5001|
___

10. Write a query to display all the customers with orders issued on date 17th August, 2012.  
    

    ![Imgur](https://i.imgur.com/lXgme14.png)  

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  

        SELECT b.*, a.cust_name
        FROM orders b, customer a
           WHERE a.customer_id=b.customer_id
           AND b.ord_date='2012-08-17';


    |ord_no	|purch_amt	|ord_date	|customer_id	|salesman_id|cust_name|
    |---|---|---|---|---|---|
    |70004	|110.50		|2012-08-17	|3009		|5003		|Geoff Cameron|
    |70011	|75.29		|2012-08-17	|3003		|5007		|Jozy Altidor|
___

11. Write a query to find the name and numbers of all salesmen who had more than one customer.  

    ![Imgur](https://i.imgur.com/GLOGcQK.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT salesman_id,name 
        FROM salesman a 
        WHERE 1 < 
            (SELECT COUNT(*) 
            FROM customer 
            WHERE salesman_id=a.salesman_id);
        
    |salesman_id	|name|
    |---|---|
    |5001		|James Hoog|
    |5002		|Nail Knite|

___

12. Write a query to find all orders with order amounts which are above-average amounts for their customers.  

    ![Imgur](https://i.imgur.com/u4S0LSc.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT * 
        FROM orders a
        WHERE purch_amt >
            (SELECT AVG(purch_amt) FROM orders b 
            WHERE b.customer_id = a.customer_id);
   
    |ord_no	|purch_amt	|ord_date	|customer_id	|salesman_id|
    |---|---|---|---|---|
    |70008	|5760.00		|2012-09-10	|3002		|5001|
    |70003	|2480.40		|2012-10-10	|3009		|5003|
    |70013	|3045.60		|2012-04-25	|3002		|5001|
    |70007	|948.50		|2012-09-10	|3005		|5002|

___

13. Write a queries to find all orders with order amounts which are on or above-average amounts for their customers.  

    ![Imgur](https://i.imgur.com/u4S0LSc.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT * 
        FROM orders a
        WHERE purch_amt >=
            (SELECT AVG(purch_amt) FROM orders b 
             WHERE b.customer_id = a.customer_id);


    |ord_no	|purch_amt	|ord_date	|customer_id	|salesman_id|
    |---|---|---|---|---|
    |70009	|270.65		|2012-09-10	|3001		|5005|
    |70005	|2400.60		|2012-07-27	|3007		|5001|
    |70008	|5760.00		|2012-09-10	|3002		|5001|
    |70010	|1983.43		|2012-10-10	|3004		|5006|
    |70003	|2480.40		|2012-10-10	|3009		|5003|
    |70011	|75.29		|2012-08-17	|3003		|5007|
    |70013	|3045.60		|2012-04-25	|3002		|5001|
    |70007	|948.50		|2012-09-10	|3005		|5002|
    |70012	|250.45		|2012-06-27	|3008		|5002|
___

14. Write a query to find the sums of the amounts from the orders table, grouped by date, eliminating all those dates where the sum was not at least 1000.00 above the maximum order amount for that date.  

    ![Imgur](https://i.imgur.com/u4S0LSc.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT ord_date, SUM (purch_amt)
        FROM orders a
        GROUP BY ord_date
        HAVING SUM (purch_amt) >
            (SELECT 1000.00 + MAX(purch_amt) 
            FROM orders b 
            WHERE a.ord_date = b.ord_date);

    |ord_date	|sum|
    |---|---|
    |2012-09-10	|6979.15|
    |2012-10-10	|4463.83|

___
15. Write a query to extract the data from the customer table if and only if one or more of the customers in the customer table are located in London.  

    ![Imgur](https://i.imgur.com/wMGHFTQ.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT customer_id, cust_name, city
        FROM customer
        WHERE EXISTS
            (SELECT *
            FROM customer 
            WHERE city='London');
    
    |customer_id	|cust_name		|city|
    |---|---|---|
    |3002		|Nick Rimando	|New York|
    |3007		|Brad Davis		|New York|
    |3005		|Graham Zusi		|California|
    |3008		|Julian Green	|London|
    |3004		|Fabian Johnson	|Paris|
    |3009		|Geoff Cameron	|Berlin|
    |3003		|Jozy Altidor	|Moscow|
    |3001		|Brad Guzan		|London|
___
16. Write a query to find the salesmen who have multiple customers. 

    ![Imgur](https://i.imgur.com/u4jFJwl.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT * 
        FROM salesman 
        WHERE salesman_id IN (
        SELECT DISTINCT salesman_id 
        FROM customer a 
        WHERE EXISTS (
            SELECT * 
            FROM customer b 
            WHERE b.salesman_id=a.salesman_id 
            AND b.cust_name<>a.cust_name));
    
    |salesman_id	|name		|city	|commission|
    |---|---|---|---|
    |5001		|James Hoog	|New York|	0.15|
    |5002		|Nail Knite	|Paris	|	0.13|
___
17. Write a query to find all the salesmen who worked for only one customer.  

    ![Imgur](https://i.imgur.com/a6I2n6R.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT * 
        FROM salesman 
        WHERE salesman_id IN (
        SELECT DISTINCT salesman_id 
        FROM customer a 
        WHERE NOT EXISTS (
            SELECT * FROM customer b 
            WHERE a.salesman_id=b.salesman_id 
            AND a.cust_name<>b.cust_name));

    |salesman_id	|name		|city	|commission|
    |---|---|---|---|
    |5005		|Pit Alex	|London	|0.11|
    |5006		|Mc Lyon		|Paris	|0.14|
    |5007		|Paul Adam	|Rome	|0.13|
    |5003		|Lauson Hen	|San Jose|0.12|
___

18. Write a query that extract the rows of all salesmen who have customers with more than one orders.  

    ![Imgur](https://i.imgur.com/9xp9rHP.png)
    ![Imgur](https://i.imgur.com/OmAjQKY.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT * 
        FROM salesman a 
        WHERE EXISTS     
        (SELECT * FROM customer b     
            WHERE a.salesman_id=b.salesman_id     
            AND 1<             
                (SELECT COUNT (*)              
                FROM orders             
                WHERE orders.customer_id =            
                b.customer_id));
    
    |salesman_id	|name	    |city		|commission|
    |---|---|---|---|
    |5001		|James Hoog	|New York	|0.15|
    |5002		|Nail Knite	|Paris		|0.13|
    |5003		|Lauson Hen	|San Jose	|0.12|

___

19. Write a query to find salesmen with all information who lives in the city where any of the customers lives. 

    ![Imgur](https://i.imgur.com/ma9l4Tn.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT *
        FROM salesman 
        WHERE city=ANY
            (SELECT city
            FROM customer);

    |salesman_id	|name		|city		|commission|
    |---|---|---|---|
    |5001		|James Hoog	|New York	|0.15|
    |5002		|Nail Knite	|Paris		|0.13|
    |5005		|Pit Alex	|London		|0.11|
    |5006		|Mc Lyon		|Paris		|0.14|

___

20. Write a query to find all the salesmen for whom there are customers that follow them. G

    ![Imgur](https://i.imgur.com/ma9l4Tn.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT *
        FROM salesman 
        WHERE city IN
            (SELECT city
            FROM customer);

    |salesman_id|name	    |city	    |commission|
    |---|---|---|---|
    |5001		|James Hoog	|New York	|0.15|
    |5002		|Nail Knite	|Paris		|0.13|
    |5005		|Pit Alex	|London		|0.11|
    |5006		|Mc Lyon		|Paris		|0.14|

___

21. Write a query to display the salesmen which name are alphabetically lower than the name of the customers. 

    ![Imgur](https://i.imgur.com/ma9l4Tn.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT *
        FROM salesman a
        WHERE EXISTS
        (SELECT *
            FROM CUSTOMER b
            WHERE  a.name  < b.cust_name);

    |salesman_id	|name		|city		|commission|
    |---|---|---|---|
    |5001		|James Hoog	|New York	|0.15|
    |5002		|Nail Knite	|Paris		|0.13|
    |5006		|Mc Lyon		|Paris		|0.14|
    |5003		|Lauson Hen	|San Jose	|0.12|

___

22. Write a query to display the customers who have a greater gradation than any customer who belongs to the alphabetically lower than the city New York. 

    ![Imgur](https://i.imgur.com/ma9l4Tn.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT *
        FROM customer
        WHERE grade > ANY
        (SELECT grade
            FROM CUSTOMER
            WHERE  city < 'New York');

    |customer_id	|cust_name		|city		    |grade	|salesman_id|
    |---|---|---|---|---|
    |3007		|Brad Davis		|New York	    |200	    |5001|
    |3005		|Graham Zusi		|California	    |200	    |5002|
    |3008		|Julian Green	|	London		|300	    |5002|
    |3004		|Fabian Johnson	|	Paris		|300	    |5006|
    |3003		|Jozy Altidor	|	Moscow		|200	    |5007|
___

23. Write a query to display all the orders that had amounts that were greater than at least one of the orders on September 10th 2012. 

    ![Imgur](https://i.imgur.com/sp8LUwS.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT *
        FROM Orders
        WHERE purch_amt > ANY
        (SELECT purch_amt
            FROM orders
            WHERE  ord_date='2012/09/10');
    
    |ord_no	|purch_amt	|ord_date	|customer_id	|salesman_id|
    |---|---|---|---|---|
    |70005	|2400.60		|2012-07-27	|3007		|	5001|
    |70008	|5760.00		|2012-09-10	|3002		|	5001|
    |70010	|1983.43		|2012-10-10	|3004		|	5006|
    |70003	|2480.40		|2012-10-10	|3009		|	5003|
    |70013	|3045.60		|2012-04-25	|3002		|	5001|
    |70007	|948.50		|2012-09-10	|3005		|	5002|
   
___

24. Write a query to find all orders with an amount smaller than any amount for a customer in London. (Using ANY keyword)  

    ![Imgur](https://i.imgur.com/FVl1755.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT *
        FROM orders
        WHERE purch_amt < ANY
        (SELECT purch_amt
            FROM orders a, customer b
            WHERE  a.customer_id=b.customer_id
            AND b.city='London');

    |ord_no	|purch_amt	|ord_date	|customer_id	|salesman_id|
    |---|---|---|---|---|
    |70002	|65.26		|2012-10-05	|3002		|5001|
    |70004	|110.50		|2012-08-17	|3009		|5003|
    |70011	|75.29		|2012-08-17	|3003		|5007|
    |70001	|150.50		|2012-10-05	|3005		|5002|
    |70012	|250.45		|2012-06-27	|3008		|5002|
___

25. Write a query to display all orders with an amount smaller than any amount for a customer in London. (Using MAX) 

    ![Imgur](https://i.imgur.com/eM0VrmF.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT *
        FROM orders
        WHERE purch_amt < 
        (SELECT MAX (purch_amt)
            FROM orders a, customer b
            WHERE  a.customer_id=b.customer_id
            AND b.city='London');

    |ord_no	|purch_amt	|ord_date	|customer_id	|salesman_id|
    |---|---|---|---|---|
    |70002	|65.26		|2012-10-05	|3002		|5001|
    |70004	|110.50		|2012-08-17	|3009		|5003|
    |70011	|75.29		|2012-08-17	|3003		|5007|
    |70001	|150.50		|2012-10-05	|3005		|5002|
    |70012	|250.45		|2012-06-27	|3008		|5002|

___

26. Write a query to display only those customers whose grade are, in fact, higher than every customer in New York. 

    ![Imgur](https://i.imgur.com/RVr2gR9.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT *
        FROM customer
        WHERE grade > ALL
        (SELECT grade
            FROM customer
            WHERE city='New York');

    |customer_id	|cust_name		|city	|grade	|salesman_id|
    |---|---|---|---|---|
    |3008		|Julian Green	|London	|300		|5002|
    |3004		|Fabian Johnson	|Paris	|300		|5006|

___

27. Write a query in sql to find the name, city, and the total sum of orders amount a salesman collects. Salesman should belong to the cities where any of the customer belongs. 

    ![Imgur](https://i.imgur.com/t77rP3h.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT salesman.name, salesman.city, subquery1.total_amt 
        FROM salesman, 
            (SELECT salesman_id, SUM(orders.purch_amt) AS total_amt 
            FROM orders 
            GROUP BY salesman_id) subquery1 
            WHERE subquery1.salesman_id = salesman.salesman_id 
            AND salesman.city 
                IN (SELECT DISTINCT city FROM customer);

    |name    |   city   | total_amt |
    |----|---|---|
    |Mc Lyon    | Paris    |   1983.43|
    |Nail Knite | Paris    |   1349.45|
    |James Hoog | New York |  11271.46|
    |Pit Alex   | London   |    270.65|


___

28. Write a query to get all the information for those customers whose grade is not as the grade of customer who belongs to the city London.  

    ![Imgur](https://i.imgur.com/PE13mHx.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT * 
        FROM customer 
        WHERE grade<> 
        ANY (
            SELECT grade 
            FROM customer 
            WHERE city='London');

    |customer_id|cust_name		|city		|grade	|salesman_id|
    |---|---|---|---|---|
    |3002		|Nick Rimando	|New York	|100	    |5001|
    |3007		|Brad Davis		|New York	|200	    |5001|
    |3005		|Graham Zusi		|California	|200	    |5002|
    |3009		|Geoff Cameron	|Berlin		|100	    |5003|
    |3003		|Jozy Altidor	|Moscow		|200	    |5007|
___
29. Write a query to find all those customers whose grade are not as the grade, belongs to the city Paris. 

    ![Imgur](https://i.imgur.com/PE13mHx.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT *
        FROM customer 
        WHERE grade NOT IN
        (SELECT grade
            FROM customer
            WHERE city='Paris');

    |customer_id	|cust_name		|city		|grade	|salesman_id|
    |---|---|---|---|---|
    |3002		|Nick Rimando	|New York	|100	    |5001|
    |3007		|Brad Davis		|New York	|200	    |5001|
    |3005		|Graham Zusi		|California	|200	    |5002|
    |3009		|Geoff Cameron	|Berlin		|100	    |5003|
    |3003		|Jozy Altidor	|Moscow		|200	    |5007|

___

30. Write a query to find all those customers who hold a different grade than any customer of the city Dallas. 

    ![Imgur](https://i.imgur.com/PE13mHx.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT *
        FROM customer 
        WHERE NOT grade = ANY
        (SELECT grade
            FROM customer
            WHERE city='Dallas');

    |customer_id|cust_name		|city		|grade|	salesman_id|
    |---|---|---|---|---|
    |3002		|Nick Rimando	|New York	|100	   | 5001|
    |3007		|Brad Davis		|New York	|200	   | 5001|
    |3005		|Graham Zusi		|California	|200	   | 5002|
    |3008		|Julian Green	|London		|300	   | 5002|
    |3004		|Fabian Johnson	|Paris		|300	   | 5006|
    |3009		|Geoff Cameron	|Berlin		|100	   | 5003|
    |3003		|Jozy Altidor	|Moscow		|200	   | 5007|
    |3001		|Brad Guzan		|London		|	   | 5005|

___

31. Write a SQL query to find the average price of each manufacturer's products along with their name.

    ![Imgur](https://i.imgur.com/9M5rosR.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT AVG(pro_price) AS "Average Price", 
        company_mast.com_name As "Company"
        FROM item_mast, company_mast
                WHERE item_mast.pro_com= company_mast.com_id
                GROUP BY company_mast.com_name;

    |Average Price		    |Company|
    |---|---|
    |5000.0000000000000000	|Samsung|
    |650.0000000000000000	|iBall|
    |1475.0000000000000000	|Epsion|
    |500.0000000000000000	|Frontech|
    |250.0000000000000000	|Zebronics|
    |3200.0000000000000000	|Asus|
___

32. Write a SQL query to display the average price of the products which is more than or equal to 350 along with their names.

    ![Imgur](https://i.imgur.com/9M5rosR.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT AVG(pro_price) AS "Average Price", 
        company_mast.com_name AS "Company"
            FROM item_mast, company_mast
                WHERE item_mast.pro_com= company_mast.com_id
                GROUP BY company_mast.com_name
                HAVING AVG(pro_price) >= 350;

    |Average Price		    |Company|
    |---|---|
    |5000.0000000000000000	|Samsung|
    |650.0000000000000000	|iBall|
    |1475.0000000000000000	|Epsion|
    |500.0000000000000000	|Frontech|
    |3200.0000000000000000	|Asus|
___

33. Write a SQL query to display the name of each company, price for their most expensive product along with their Name.


    ![Imgur](https://i.imgur.com/9M5rosR.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT P.pro_name AS "Product Name", 
            P.pro_price AS "Price", 
            C.com_name AS "Company"
        FROM item_mast P, company_mast C
        WHERE P.pro_com = C.com_id
            AND P.pro_price =
            (
            SELECT MAX(P.pro_price)
                FROM item_mast P
                WHERE P.pro_com = C.com_id
            );

    |Product Name    |Price	    |Company|
    |---|---|---|
    |Monitor		    |5000.00		|Samsung|
    |DVD drive	    |900.00		|iBall|
    |Printer		    |2600.00		|Epsion|
    |ZIP drive	    |250.00		|Zebronics|
    |Mother Board	|3200.00		|Asus|
    |Speaker		    |550.00		|Frontech|
___

34. Write a query in SQL to find all the details of employees whose last name is Gabriel or Dosio.

    ![Imgur](https://i.imgur.com/97lHr4P.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT * 
        FROM emp_details
        WHERE emp_lname 
        IN ('Gabriel' , 'Dosio');

    |emp_idno	|emp_fname	|emp_lname	|emp_dept|
    |---|---|---|---|
    |843795		|Enric		|Dosio		|57|
    |748681		|Henrey		|Gabriel		|47|

___

35. Write a query in SQL to display all the details of employees who works in department 89 or 63.

    ![Imgur](https://i.imgur.com/ZacgzmS.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT * 
        FROM emp_details
        WHERE emp_dept IN (89,63);  

    |emp_idno	|emp_fname	|emp_lname	|emp_dept|
    |---|---|---|---|
    |526689		|Carlos		|Snares		|63|
    |328717		|Jhon		|Snares		|63|
    |733843		|Mario		|Saule		|63| 
___

36. Write a query in SQL to display the first name and last name of employees working for the department which allotment amount is more than Rs.50000.

    ![Imgur](https://i.imgur.com/ZacgzmS.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT emp_fname, emp_lname 
        FROM emp_details
        WHERE emp_dept IN
        (SELECT dpt_code 
            FROM emp_department 
            WHERE dpt_allotment > 50000);

    |emp_fname	|emp_lname|
    |---|---|
    |Alan		|Snappy|
    |Maria		|Foster|
    |Michale		|Robbin|
    |Enric		|Dosio|
    |Joseph		|Dosni|
    |Zanifer		|Emily|
    |Kuleswar	|Sitaraman|
    |Henrey		|Gabriel|
    |Alex		|Manuel|
    |George		|Mardy|
___

37. Write a query in SQL to find the departments which sanction amount is larger than the average sanction amount of all the departments.


    ![Imgur](https://i.imgur.com/JUrsR2v.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT *
        FROM emp_department
        WHERE dpt_allotment >
            (
            SELECT AVG(dpt_allotment)
            FROM emp_department
            );
    
    |dpt_code	|dpt_name	|dpt_allotment|
    |---|---|---|
    |47	        |HR	        |240000|
___
38. Write a query in SQL to find the names of departments with more than two employees are working.


    ![Imgur](https://i.imgur.com/3v1R4sn.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT dpt_name FROM emp_department
        WHERE dpt_code IN
            (
            SELECT emp_dept
            FROM emp_details
            GROUP BY emp_dept
            HAVING COUNT(*) >2
            );

    |dpt_name|
    |---|
    |IT|
    |HR|
    |Finance|
___

39. Write a query in SQL to find the first name and last name of employees working for departments which sanction amount is second lowest.


    ![Imgur](https://i.imgur.com/3v1R4sn.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT emp_fname, emp_lname 
        FROM emp_details 
        WHERE emp_dept IN (
            SELECT dpt_code
            FROM emp_department 
                WHERE dpt_allotment= (
                    SELECT MIN(dpt_allotment)
                    FROM emp_department 
                    WHERE dpt_allotment >
                (SELECT MIN(dpt_allotment) 
                    FROM emp_department )
                )
            );

    |emp_fname	|emp_lname|
    |---|---|
    |Alan		|Snappy|
    |George		|Mardy|
___