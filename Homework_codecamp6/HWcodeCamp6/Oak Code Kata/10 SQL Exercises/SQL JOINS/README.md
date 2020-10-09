# SQL Exercises
## SQL JOINS
1. Write a SQL statement to prepare a list with salesman name, customer name and their cities for the salesmen and customer who belongs to the same city.    

    ![Imgur](https://i.imgur.com/pv6oghU.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT salesman.name AS "Salesman",   
        customer.cust_name, customer.city   
        FROM salesman, customer     
        WHERE salesman.city = customer.city;  

    |Salesman	|cust_name	    |city|
    |---|---|---|
    |James Hoog	|Nick Rimando	|New York|
    |James Hoog	|Brad Davis	    |New York|
    |Pit Alex	|Julian Green	|London|
    |Mc Lyon		|Fabian Johnson	|Paris|
    |Nail Knite	|Fabian Johnson	|Paris|
    |Pit Alex	|Brad Guzan	    |London|
 
___
2. Write a SQL statement to make a list with order no, purchase amount, customer name and their cities for those orders which order amount between 500 and 2000.  

    ![Imgur](https://i.imgur.com/xsHwqmT.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT a.ord_no, a.purch_amt, b.cust_name, b.city   
        FROM orders a ,customer b   
        WHERE a.customer_id = b.customer_id  
        AND a.purch_amt   
        BETWEEN 500 AND 2000;

    |ord_no|	purch_amt|	cust_name|	city|
    |---|---|---|---|
    |70007|	948.50|	Graham Zusi|	California|
    |70010|	1983.43|	Fabian Johnson|	Paris|
___
3. Write a SQL statement to know which salesman are working for which customer.  

    ![Imgur](https://i.imgur.com/vKaPNRi.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT a.cust_name AS "Customer Name", a.city,   
        b.name AS "Salesman", b.commission  
        FROM customer a  
        INNER JOIN salesman b   
        ON a.salesman_id = b.salesman_id;  

    |Customer Name	|city	    |Salesman	|commission|
    |---|---|---|---|
    |Nick Rimando	|New York	|James Hoog	|0.15|
    |Brad Davis	    |New York	|James Hoog	|0.15|
    |Graham Zusi	    |California	|Nail Knite	|0.13|
    |Julian Green	|London	    |Nail Knite	|0.13|
    |Fabian Johnson	|Paris	    |Mc Lyon	|0.14|
    |Geoff Cameron	|Berlin	    |Lauson Hen	|0.12|
    |Jozy Altidor	|Moscow	    |Paul Adam	|0.13|
    |Brad Guzan	    |London	    |Pit Alex	|0.11|
___
4. Write a SQL statement to find the list of customers who appointed a salesman for their jobs who gets a commission from the company is more than 12%.   

    ![Imgur](https://i.imgur.com/l3FojlZ.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT a.cust_name AS "Customer Name",   
        a.city, b.name AS "Salesman", b.commission   
        FROM customer a   
        INNER JOIN salesman b   
        ON a.salesman_id = b.salesman_id   
        WHERE b.commission > .12;

    |Customer Name	|city	    |Salesman	|commission|
    |---|---|---|---|
    |Nick Rimando	|New York	|James Hoog	|0.15|
    |Brad Davis	    |New York	|James Hoog	|0.15|
    |Graham Zusi	    |California	|Nail Knite	|0.13|
    |Julian Green	|London	    |Nail Knite	|0.13|
    |Fabian Johnson	|Paris	    |Mc Lyon	    |0.14|
    |Jozy Altidor	|Moscow	    |Paul Adam	|0.13|
___
5. Write a SQL statement to find the list of customers who appointed a salesman for their jobs who does not live in the same city where their customer lives, and gets a commission is above 12% .   

    ![Imgur](https://i.imgur.com/dxK6lUH.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT a.cust_name AS "Customer Name", a.city,   
        b.name AS "Salesman", b.city,b.commission  
        FROM customer a  
        INNER JOIN salesman b   
        ON a.salesman_id = b.salesman_id   
        WHERE b.commission > .12   
        AND a.city<>b.city;

    |Customer Name|	city|	Salesman|	commission|
    |---|---|---|---|
    |Graham Zusi|	Paris|	Nail Knite|	0.13|
    |Julian Green|	Paris|	Nail Knite|	0.13|
    |Jozy Altidor|	Rome|	Paul Adam|	0.13|
___
6. Write a SQL statement to find the details of a order i.e. order number, order date, amount of order, which customer gives the order and which salesman works for that customer and how much commission he gets for an order.   

    ![Imgur](https://i.imgur.com/vtMVDND.png)
    ![Imgur](https://i.imgur.com/4uYPvQU.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT a.ord_no, a.ord_date, a.purch_amt,  
        b.cust_name AS "Customer Name", b.grade,   
        c.name AS "Salesman", c.commission 
        FROM orders a   
        INNER JOIN customer b   
        ON a.customer_id = b.customer_id   
        INNER JOIN salesman c   
        ON a.salesman_id = c.salesman_id;

    |ord_no	|ord_date	|purch_amt	|Customer Name	|grade	|Salesman	|commission|
    |---|---|---|---|---|---|---|
    |70009	|2012-09-10	|270.65	    |Brad Guzan		|        |Pit Alex	|0.11|
    |70002	|2012-10-05	|65.26	    |Nick Rimando	|100	    |James Hoog	|0.15|
    |70004	|2012-08-17	|110.50	    |Geoff Cameron	|100	    |Lauson Hen	|0.12|
    |70005	|2012-07-27	|2400.60	    |Brad Davis	    |200	    |James Hoog	|0.15|
    |70008	|2012-09-10	|5760.00	    |Nick Rimando	|100	    |James Hoog	|0.15|
    |70010	|2012-10-10	|1983.43	    |Fabian Johnson	|300	    |Mc Lyon	    |0.14|
    |70003	|2012-10-10	|2480.40	    |Geoff Cameron	|100	    |Lauson Hen	|0.12|
    |70011	|2012-08-17	|75.29	    |Jozy Altidor	|200	    |Paul Adam	|0.13|
    |70013	|2012-04-25	|3045.60	    |Nick Rimando	|100	    |James Hoog	|0.15|
    |70001	|2012-10-05	|150.50	    |Graham Zusi	    |200	    |Nail Knite	|0.13|
    |70007	|2012-09-10	|948.50	    |Graham Zusi	    |200	    |Nail Knite	|0.13|
    |70012	|2012-06-27	|250.45	    |Julian Green	|300	    |Nail Knite	|0.13|

___
7. Write a SQL statement to make a join on the tables salesman, customer and orders in such a form that the same column of each table will appear once and only the relational rows will come.  

    ![Imgur](https://i.imgur.com/vr7Gzl4.png)
    ![Imgur](https://i.imgur.com/Xsf0V7j.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT *   
        FROM orders  
        NATURAL JOIN customer    
        NATURAL JOIN salesman; 

    |salesman_id	|city	    |customer_id	|ord_no	|purch_amt	|ord_date	|cust_name	    |grade	|name	    |commission|
    |---|---|---|---|---|---|---|---|---|
    |5005	    |London	    |3001	    |70009	|270.65	    |2012-09-10	|Brad Guzan	    |	    |Pit Alex	|0.11|
    |5001	    |New York	|3002	    |70002	|65.26	    |2012-10-05	|Nick Rimando    |100	    |James Hoog	|0.15|
    |5001	    |New York	|3007	    |70005	|2400.60	    |2012-07-27	|Brad Davis	    |200	    |James Hoog	|0.15|
    |5001	    |New York	|3002	    |70008	|5760.00	    |2012-09-10	|Nick Rimando	|100	    |James Hoog	|0.15|
    |5006	    |Paris	    |3004	    |70010	|1983.43	    |2012-10-10	|Fabian Johnson	|300	    |Mc Lyon	    |0.14|
    |5001	    |New York	|3002	    |70013	|3045.60	    |2012-04-25	|Nick Rimando	|100	    |James Hoog	|0.15|

___
8. Write a SQL statement to make a list in ascending order for the customer who works either through a salesman or by own.   

    ![Imgur](https://i.imgur.com/ndf2rSo.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT a.cust_name, a.city, a.grade,   
        b.name AS "Salesman", b.city   
        FROM customer a   
        LEFT JOIN salesman b   
        ON a.salesman_id = b.salesman_id   
        order by a.customer_id;

    |cust_name	    |city	    |grade	|Salesman|
    |---|---|---|---|
    |Brad Guzan	    |London		|Pit     |Alex|
    |Nick Rimando	|New York	|100	    |James Hoog|
    |Jozy Altidor	|Rome	    |200	    |Paul Adam|
    |Fabian Johnson	|Paris	    |300	    |Mc Lyon|
    |Graham Zusi	    |Paris	    |200	    |Nail Knite|
    |Brad Davis	    |New York    |	    |200	James Hoog|
    |Julian Green	|Paris	    |300	    |Nail Knite|
    |Geoff Cameron	|San Jose	|100	    |Lauson Hen|
___
9. Write a SQL statement to make a list in ascending order for the customer who holds a grade less than 300 and works either through a salesman or by own. 

    ![Imgur](https://i.imgur.com/08Mw7xs.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT a.cust_name, a.city, a.grade,   
        b.name AS "Salesman", b.city   
        FROM customer a   
        LEFT OUTER JOIN salesman b   
        ON a.salesman_id = b.salesman_id   
        WHERE a.grade < 300   
        ORDER BY a.customer_id;

    |cust_name	    |city	  |  grade	|Salesman|
    |---|---|---|---|
    |Nick Rimando	|New York	|100	    |James Hoog|
    |Jozy Altidor	|Rome	    |200	    |Paul Adam|
    |Graham Zusi	    |Paris	    |200	    |Nail Knite|
    |Brad Davis	    |New York	|200	    |James Hoog|
    |Geoff Cameron	|San Jose	|100	    |Lauson Hen|

___
10. Write a SQL statement to make a report with customer name, city, order number, order date, and order amount in ascending order according to the order date to find that either any of the existing customers have placed no order or placed one or more orders.  

    ![Imgur](https://i.imgur.com/fPb4nXm.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT a.cust_name, a.city, b.ord_no,  
        b.ord_date, b.purch_amt AS "Order Amount"   
        FROM customer a   
        LEFT OUTER JOIN orders b   
        ON a.customer_id = b.customer_id   
        order by b.ord_date;

    |cust_name	    |city		|ord_no	|ord_date	|Order Amount|
    |---|---|---|---|---|
    |Nick Rimando	|New York	|70013	|2012-04-25	|3045.60|
    |Julian Green	|London		|70012	|2012-06-27	|250.45|
    |Brad Davis	    |New York	|70005	|2012-07-27	|2400.60|
    |Jozy Altidor	|Moscow		|70011	|2012-08-17	|75.29|
    |Geoff Cameron	|Berlin		|70004	|2012-08-17	|110.50|
    |Brad Guzan	    |London		|70009	|2012-09-10	|270.65|
    |Nick Rimando	|New York	|70008	|2012-09-10	|5760.00|
    |Graham Zusi	    |California	|70007	|2012-09-10	|948.50|
    |Graham Zusi	    |California	|70001	|2012-10-05	|150.50|
    |Nick Rimando	|New York	|70002	|2012-10-05	|65.26|
    |Fabian Johnson	|Paris		|70010	|2012-10-10	|1983.43|
    |Geoff Cameron	|Berlin		|70003	|2012-10-10	|2480.40|
___
11. Write a SQL statement to make a report with customer name, city, order number, order date, order amount salesman name and commission to find that either any of the existing customers have placed no order or placed one or more orders by their salesman or by own.  

    ![Imgur](https://i.imgur.com/78nvvQX.png)
    ![Imgur](https://i.imgur.com/jqZ684Z.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT a.cust_name, a.city, b.ord_no,  
        b.ord_date, b.purch_amt AS "Order Amount",   
        c.name, c.commission   
        FROM customer a   
        LEFT OUTER JOIN orders b   
        ON a.customer_id = b.customer_id   
        LEFT OUTER JOIN salesman c   
        ON c.salesman_id = b.salesman_id;

    |cust_name	    |city		|ord_no	|ord_date	|Order Amount	|name		|commission|
    |---|---|---|---|---|---|---|
    |Brad Guzan	    |London		|70009	|2012-09-10	|270.65		    |Pit Alex	|0.11|
    |Nick Rimando	|New York	|70002	|2012-10-05	|65.26		    |James Hoog	|0.15|
    |Geoff Cameron	|Berlin		|70004	|2012-08-17	|110.50		    |Lauson Hen	|0.12|
    |Brad Davis	    |New York	|70005	|2012-07-27	|2400.60		    |James Hoog	|0.15|
    |Nick Rimando	|New York	|70008	|2012-09-10	|5760.00		    |James Hoog	|0.15|
    |Fabian Johnson	|Paris		|70010	|2012-10-10	|1983.43		    |Mc Lyon		|0.14|
    |Geoff Cameron	|Berlin		|70003	|2012-10-10	|2480.40		    |Lauson Hen	|0.12|
    |Jozy Altidor	|Moscow		|70011	|2012-08-17	|75.29		    |Paul Adam	|0.13|
    |Nick Rimando	|New York	|70013	|2012-04-25	|3045.60		    |James Hoog	|0.15|
    |Graham Zusi	    |California	|70001	|2012-10-05	|150.50		    |Nail Knite	|0.13|
    |Graham Zusi	    |California	|70007	|2012-09-10	|948.50		    |Nail Knite	|0.13|
    |Julian Green	|London		|70012	|2012-06-27	|250.45		    |Nail Knite	|0.13|
___
12. Write a SQL statement to make a list in ascending order for the salesmen who works either for one or more customer or not yet join under any of the customers.  

    ![Imgur](https://i.imgur.com/7EwUN3Z.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT a.cust_name, a.city, a.grade,   
        b.name AS "Salesman", b.city   
        FROM customer a   
        RIGHT OUTER JOIN salesman b   
        ON b.salesman_id = a.salesman_id   
        ORDER BY b.salesman_id;

    |cust_name	    |city		|grade	|Salesman	|city|
    |---|---|---|---|---|
    |Brad Davis	    |New York	|200	    |James Hoog	|New York|
    |Nick Rimando	|New York	|100	    |James Hoog	|New York|
    |Graham Zusi	    |California	|200	    |Nail Knite	|Paris|
    |Julian Green	|London		|300	    |Nail Knite	|Paris|
    |Geoff Cameron	|Berlin		|100	    |Lauson Hen	|San Jose|
    |Brad Guzan	    |London		|	    |Pit Alex	|London|
    |Fabian Johnson	|Paris		|300	    |Mc Lyon		|Paris||
    |Jozy Altidor	|Moscow		|200	    |Paul Adam	|Rome|

___
13. Write a SQL statement to make a list for the salesmen who works either for one or more customer or not yet join under any of the customers who placed either one or more orders or no order to their supplier.  

    ![Imgur](https://i.imgur.com/zNvqJEr.png)
    ![Imgur](https://i.imgur.com/9jZNHF9.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT a.cust_name, a.city, a.grade,   
        b.name AS "Salesman",   
        c.ord_no, c.ord_date, c.purch_amt   
        FROM customer a   
        RIGHT OUTER JOIN salesman b   
        ON b.salesman_id = a.salesman_id   
        RIGHT OUTER JOIN orders c   
        ON c.customer_id = a.customer_id;

    |cust_name	    |city		|grade	|Salesman	|ord_no	|ord_date	|purch_amt|
    |---|---|---|---|---|---|---|
    |Brad Guzan	    |London		|	    |Pit Alex	|70009	|2012-09-10	|270.65|
    |Nick Rimando	|New York	|100	    |James Hoog	|70002	|2012-10-05	|65.26|
    |Geoff Cameron	|Berlin		|100	    |Lauson Hen	|70004	|2012-08-17	|110.50|
    |Brad Davis	    |New York	|200	    |James Hoog	|70005	|2012-07-27	|2400.60|
    |Nick Rimando	|New York	|100	    |James Hoog	|70008	|2012-09-10	|5760.00|
    |Fabian Johnson	|Paris		|300	    |Mc Lyon		|70010	|2012-10-10	|1983.43|
    |Geoff Cameron	|Berlin		|100	    |Lauson Hen	|70003	|2012-10-10	|2480.40|
    |Jozy Altidor	|Moscow		|200	    |Paul Adam	|70011	|2012-08-17	|75.29|
    |Nick Rimando	|New York	|100	    |James Hoog	|70013	|2012-04-25	|3045.60|
    |Graham Zusi	    |California	|200	    |Nail Knite	|70001	|2012-10-05	|150.50|
    |Graham Zusi	    |California	|200	    |Nail Knite	|70007	|2012-09-10	|948.50|
    |Julian Green	|London		|300	    |Nail Knite	|70012	|2012-06-27	|250.45|
___
14. Write a SQL statement to make a list for the salesmen who either work for one or more customers or yet to join any of the customer. The customer may have placed, either one or more orders on or above order amount 2000 and must have a grade, or he may not have placed any order to the associated supplier.  

    ![Imgur](https://i.imgur.com/SWqOL2j.png)
    ![Imgur](https://i.imgur.com/pDlRSju.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT a.cust_name, a.city, a.grade,   
        b.name AS "Salesman",   
        c.ord_no, c.ord_date, c.purch_amt   
        FROM customer a   
        RIGHT OUTER JOIN salesman b   
        ON b.salesman_id = a.salesman_id   
        LEFT OUTER JOIN orders c   
        ON c.customer_id = a.customer_id   
        WHERE c.purch_amt >= 2000   
        AND a.grade IS NOT NULL;  

    |cust_name	    |city		|grade	|Salesman	|ord_no	|ord_date	|purch_amt|
    |---|---|---|---|---|---|---|
    |Nick Rimando	|New York	|100	    |James Hoog	|70013	|2012-04-25	|3045.60|
    |Nick Rimando	|New York	|100	    |James Hoog	|70008	|2012-09-10	|5760.00|
    |Brad Davis	    |New York	|200	    |James Hoog	|70005	|2012-07-27	|2400.60|
    |Geoff Cameron	|Berlin		|100	    |Lauson Hen	|70003	|2012-10-10	|2480.40|

___
15. Write a SQL statement to make a report with customer name, city, order no. order date, purchase amount for those customers from the existing list who placed one or more orders or which order(s) have been placed by the customer who is not on the list.  

    ![Imgur](https://i.imgur.com/r1i0Q8U.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT a.cust_name, a.city, b.ord_no,  
        b.ord_date, b.purch_amt AS "Order Amount"   
        FROM customer a  
        FULL OUTER JOIN orders b   
        ON a.customer_id = b.customer_id;  

    |cust_name	    |city		|ord_no	|ord_date	|Order Amount|
    |---|---|---|---|---|---|
    |Brad Guzan	    |London		|70009	|2012-09-10	|270.65|
    |Nick Rimando	|New York	|70002	|2012-10-05	|65.26|
    |Geoff Cameron	|Berlin		|70004	|2012-08-17	|110.50|
    |Brad Davis	    |New York	|70005	|2012-07-27	|2400.60|
    |Nick Rimando	|New York	|70008	|2012-09-10	|5760.00|
    |Fabian Johnson	|Paris		|70010	|2012-10-10	|1983.43|
    |Geoff Cameron	|Berlin		|70003	|2012-10-10	|2480.40|
    |Jozy Altidor	|Moscow		|70011	|2012-08-17	|75.29|
    |Nick Rimando	|New York	|70013	|2012-04-25	|3045.60|
    |Graham Zusi	    |California	|70001	|2012-10-05	|150.50|
    |Graham Zusi	    |California	|70007	|2012-09-10	|948.50|
    |Julian Green	|London		|70012	|2012-06-27	|250.45|

___
16. Write a SQL statement to make a report with customer name, city, order no. order date, purchase amount for only those customers on the list who must have a grade and placed one or more orders or which order(s) have been placed by the customer who is neither in the list not have a grade.  

    ![Imgur](https://i.imgur.com/06FXxxM.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT a.cust_name, a.city, b.ord_no,  
        b.ord_date,b.purch_amt AS "Order Amount"   
        FROM customer a   
        FULL OUTER JOIN orders b   
        ON a.customer_id=b.customer_id   
        WHERE a.grade IS NOT NULL;

    |cust_name	    |city		|ord_no	|ord_date	|Order Amount|
    |---|---|---|---|---|---|
    |Brad Guzan	    |London		|70009	|2012-09-10	|270.65|
    |Nick Rimando	|New York	|70002	|2012-10-05	|65.26|
    |Geoff Cameron	|Berlin		|70004	|2012-08-17	|110.50|
    |Brad Davis	    |New York	|70005	|2012-07-27	|2400.60|
    |Nick Rimando	|New York	|70008	|2012-09-10	|5760.00|
    |Fabian Johnson	|Paris		|70010	|2012-10-10	|1983.43|
    |Geoff Cameron	|Berlin		|70003	|2012-10-10	|2480.40|
    |Jozy Altidor	|Moscow		|70011	|2012-08-17	|75.29|
    |Nick Rimando	|New York	|70013	|2012-04-25	|3045.60|
    |Graham Zusi	    |California	|70001	|2012-10-05	|150.50|
    |Graham Zusi	    |California	|70007	|2012-09-10	|948.50|
    |Julian Green	|London		|70012	|2012-06-27	|250.45|

___
17. Write a SQL statement to make a cartesian product between salesman and customer i.e. each salesman will appear for all customer and vice versa.  

    ![Imgur](https://i.imgur.com/4j9zhdK.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT *   
        FROM salesman a   
        CROSS JOIN customer b;  

    |salesman_id	|name	    |city		|commission	|customer_id	|cust_name	    |city		|grade	|salesman_id|
    |---|---|---|---|---|---|---|---|---|
    |5001	    |James Hoog	|New York	|0.15		|3002		|Nick Rimando	|New York	|100	    |5001|
    |5002	    |Nail Knite	|Paris		|0.13		|3002		|Nick Rimando	|New York	|100	    |5001|
    |5005	    |Pit Alex	|London		|0.11		|3002		|Nick Rimando	|New York	|100	    |5001|
    |5006	    |Mc Lyon		|Paris		|0.14		|3002		|Nick Rimando	|New York	|100	    |5001|
    |5007	    |Paul Adam	|Rome		|0.13		|3002		|Nick Rimando	|New York	|100	    |5001|
    |5003	    |Lauson Hen	|San Jose	|0.12		|3002		|Nick Rimando	|New York	|100	    |5001|
    |5001	    |James Hoog	|New York	|0.15		|3007		|Brad Davis	    |New York	|200	    |5001|
    |5002	    |Nail Knite	|Paris		|0.13		|3007		|Brad Davis	    |New York	|200	    |5001|
    |5005	    |Pit Alex	|London		|0.11		|3007		|Brad Davis	    |New York	|200	    |5001|
    |5006	    |Mc Lyon		|Paris		|0.14		|3007		|Brad Davis	    |New York	|200	    |5001|
    |5007	    |Paul Adam	|Rome		|0.13		|3007		|Brad Davis	    |New York	|200	    |5001|
    |5003	    |Lauson Hen	|San Jose	|0.12		|3007		|Brad Davis	    |New York	|200	    |5001|
    |5001	    |James Hoog	|New York	|0.15		|3005		|Graham Zusi	    |California	|200	    |5002|
    |5002	    |Nail Knite	|Paris		|0.13		|3005		|Graham Zusi	    |California	|200	    |5002|
    |5005	    |Pit Alex	|London		|0.11		|3005		|Graham Zusi	    |California	|200	    |5002|
    |5006	    |Mc Lyon		|Paris		|0.14		|3005		|Graham Zusi	    |California	|200	    |5002|
    |5007	    |Paul Adam	|Rome		|0.13		|3005		|Graham Zusi	    |California	|200	    |5002|
    |5003	    |Lauson Hen	|San Jose	|0.12		|3005		|Graham Zusi	    |California	|200	    |5002|
    |5001	    |James Hoog	|New York	|0.15		|3008		|Julian Green	|London		|300	    |5002|
    |5002	    |Nail Knite	|Paris		|0.13		|3008		|Julian Green	|London		|300	    |5002|
    |5005	    |Pit Alex	|London		|0.11		|3008		|Julian Green	|London		|300	    |5002|
    |5006	    |Mc Lyon		|Paris		|0.14		|3008		|Julian Green	|London		|300	    |5002|
    |5007	    |Paul Adam	|Rome		|0.13		|3008		|Julian Green	|London		|300	    |5002|
    |5003	    |Lauson Hen	|San Jose	|0.12		|3008		|Julian Green	|London		|300	    |5002|
    |5001	    |James Hoog	|New York	|0.15		|3004		|Fabian Johnson	|Paris		|300	    |5006|
    |5002	    |Nail Knite	|Paris		|0.13		|3004		|Fabian Johnson	|Paris		|300	    |5006|
    |5005	    |Pit Alex	|London		|0.11		|3004		|Fabian Johnson	|Paris		|300	    |5006|
    |5006	    |Mc Lyon		|Paris		|0.14		|3004		|Fabian Johnson	|Paris		|300	    |5006|
    |5007	    |Paul Adam	|Rome		|0.13		|3004		|Fabian Johnson	|Paris		|300	    |5006|
    |5003	    |Lauson Hen	|San Jose	|0.12		|3004		|Fabian Johnson	|Paris		|300	    |5006|
    |5001	    |James Hoog	|New York	|0.15		|3009		|Geoff Cameron	|Berlin		|100	    |5003|
    |5002	    |Nail Knite	|Paris		|0.13		|3009		|Geoff Cameron	|Berlin		|100	    |5003|
    |5005	    |Pit Alex	|London		|0.11		|3009		|Geoff Cameron	|Berlin		|100	    |5003|
    |5006	    |Mc Lyon		|Paris		|0.14		|3009		|Geoff Cameron	|Berlin		|100	    |5003|
    |5007	    |Paul Adam	|Rome		|0.13		|3009		|Geoff Cameron	|Berlin		|100	    |5003|
    |5003	    |Lauson Hen	|San Jose	|0.12		|3009		|Geoff Cameron	|Berlin		|100	    |5003|
    |5001	    |James Hoog	|New York	|0.15		|3003		|Jozy Altidor	|Moscow		|200	    |5007|
    |5002	    |Nail Knite	|Paris		|0.13		|3003		|Jozy Altidor	|Moscow		|200	    |5007|
    |5005	    |Pit Alex	|London		|0.11		|3003		|Jozy Altidor	|Moscow		|200	    |5007|
    |5006	    |Mc Lyon		|Paris		|0.14		|3003		|Jozy Altidor	|Moscow		|200	    |5007|
    |5007	    |Paul Adam	|Rome		|0.13		|3003		|Jozy Altidor	|Moscow		|200	    |5007|
    |5003	    |Lauson Hen	|San Jose	|0.12		|3003		|Jozy Altidor	|Moscow		|200	    |5007|
    |5001	    |James Hoog	|New York	|0.15		|3001		|Brad Guzan	    |London		|	    |5005|
    |5002	    |Nail Knite	|Paris		|0.13		|3001		|Brad Guzan	    |London		|	    |5005|
    |5005	    |Pit Alex	|London		|0.11		|3001		|Brad Guzan	    |London		|	    |5005|
    |5006	    |Mc Lyon		|Paris		|0.14		|3001		|Brad Guzan	    |London		|	    |5005|
    |5007	    |Paul Adam	|Rome		|0.13		|3001		|Brad Guzan	    |London		|	    |5005|
    |5003	    |Lauson Hen	|San Jose	|0.12		|3001		|Brad Guzan	    |London		|	    |5005|
___
18. Write a SQL statement to make a cartesian product between salesman and customer i.e. each salesman will appear for all customer and vice versa for that salesman who belongs to a city.  

    ![Imgur](https://i.imgur.com/kkRwu8u.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT *   
        FROM salesman a   
        CROSS JOIN customer b   
        WHERE a.city IS NOT NULL;

    |salesman_id	|name	    |city		|commission	|customer_id	|cust_name	    |city		|grade	|salesman_id|
    |---|---|---|---|---|---|---|---|---|
    |5001	    |James Hoog	|New York	|0.15		|3002		|Nick Rimando	|New York	|100	    |5001|
    |5002	    |Nail Knite	|Paris		|0.13		|3002		|Nick Rimando	|New York	|100	    |5001|
    |5005	    |Pit Alex	|London		|0.11		|3002		|Nick Rimando	|New York	|100	    |5001|
    |5006	    |Mc Lyon		|Paris		|0.14		|3002		|Nick Rimando	|New York	|100	    |5001|
    |5007	    |Paul Adam	|Rome		|0.13		|3002		|Nick Rimando	|New York	|100	    |5001|
    |5003	    |Lauson Hen	|San Jose	|0.12		|3002		|Nick Rimando	|New York	|100	    |5001|
    |5001	    |James Hoog	|New York	|0.15		|3007		|Brad Davis	    |New York	|200	    |5001|
    |5002	    |Nail Knite	|Paris		|0.13		|3007		|Brad Davis	    |New York	|200	    |5001|
    |5005	    |Pit Alex	|London		|0.11		|3007		|Brad Davis	    |New York	|200	    |5001|
    |5006	    |Mc Lyon		|Paris		|0.14		|3007		|Brad Davis	    |New York	|200	    |5001|
    |5007	    |Paul Adam	|Rome		|0.13		|3007		|Brad Davis	    |New York	|200	    |5001|
    |5003	    |Lauson Hen	|San Jose	|0.12		|3007		|Brad Davis	    |New York	|200	    |5001|
    |5001	    |James Hoog	|New York	|0.15		|3005		|Graham Zusi	    |California	|200	    |5002|
    |5002	    |Nail Knite	|Paris		|0.13		|3005		|Graham Zusi	    |California	|200	    |5002|
    |5005	    |Pit Alex	|London		|0.11		|3005		|Graham Zusi	    |California	|200	    |5002|
    |5006	    |Mc Lyon		|Paris		|0.14		|3005		|Graham Zusi	    |California	|200	    |5002|
    |5007	    |Paul Adam	|Rome		|0.13		|3005		|Graham Zusi	    |California	|200	    |5002|
    |5003	    |Lauson Hen	|San Jose	|0.12		|3005		|Graham Zusi	    |California	|200	    |5002|
    |5001	    |James Hoog	|New York	|0.15		|3008		|Julian Green	|London		|300	    |5002|
    |5002	    |Nail Knite	|Paris		|0.13		|3008		|Julian Green	|London		|300	    |5002|
    |5005	    |Pit Alex	|London		|0.11		|3008		|Julian Green	|London		|300	    |5002|
    |5006	    |Mc Lyon		|Paris		|0.14		|3008		|Julian Green	|London		|300	    |5002|
    |5007	    |Paul Adam	|Rome		|0.13		|3008		|Julian Green	|London		|300	    |5002|
    |5003	    |Lauson Hen	|San Jose	|0.12		|3008		|Julian Green	|London		|300	    |5002|
    |5001	    |James Hoog	|New York	|0.15		|3004		|Fabian Johnson	|Paris		|300	    |5006|
    |5002	    |Nail Knite	|Paris		|0.13		|3004		|Fabian Johnson	|Paris		|300	    |5006|
    |5005	    |Pit Alex	|London		|0.11		|3004		|Fabian Johnson	|Paris		|300	    |5006|
    |5006	    |Mc Lyon		|Paris		|0.14		|3004		|Fabian Johnson	|Paris		|300	    |5006|
    |5007	    |Paul Adam	|Rome		|0.13		|3004		|Fabian Johnson	|Paris		|300	    |5006|
    |5003	    |Lauson Hen	|San Jose	|0.12		|3004		|Fabian Johnson	|Paris		|300	    |5006|
    |5001	    |James Hoog	|New York	|0.15		|3009		|Geoff Cameron	|Berlin		|100	    |5003|
    |5002	    |Nail Knite	|Paris		|0.13		|3009		|Geoff Cameron	|Berlin		|100	    |5003|
    |5005	    |Pit Alex	|London		|0.11		|3009		|Geoff Cameron	|Berlin		|100	    |5003|
    |5006	    |Mc Lyon		|Paris		|0.14		|3009		|Geoff Cameron	|Berlin		|100	    |5003|
    |5007	    |Paul Adam	|Rome		|0.13		|3009		|Geoff Cameron	|Berlin		|100	    |5003|
    |5003	    |Lauson Hen	|San Jose	|0.12		|3009		|Geoff Cameron	|Berlin		|100	    |5003|
    |5001	    |James Hoog	|New York	|0.15		|3003		|Jozy Altidor	|Moscow		|200	    |5007|
    |5002	    |Nail Knite	|Paris		|0.13		|3003		|Jozy Altidor	|Moscow		|200	    |5007|
    |5005	    |Pit Alex	|London		|0.11		|3003		|Jozy Altidor	|Moscow		|200	    |5007|
    |5006	    |Mc Lyon		|Paris		|0.14		|3003		|Jozy Altidor	|Moscow		|200	    |5007|
    |5007	    |Paul Adam	|Rome		|0.13		|3003		|Jozy Altidor	|Moscow		|200	    |5007|
    |5003	    |Lauson Hen	|San Jose	|0.12		|3003		|Jozy Altidor	|Moscow		|200	    |5007|
    |5001	    |James Hoog	|New York	|0.15		|3001		|Brad Guzan	    |London		|	    |5005|
    |5002	    |Nail Knite	|Paris		|0.13		|3001		|Brad Guzan	    |London		|	    |5005|
    |5005	    |Pit Alex	|London		|0.11		|3001		|Brad Guzan	    |London		|	    |5005|
    |5006	    |Mc Lyon		|Paris		|0.14		|3001		|Brad Guzan	    |London		|	    |5005|
    |5007	    |Paul Adam	|Rome		|0.13		|3001		|Brad Guzan	    |London		|	    |5005|
    |5003	    |Lauson Hen	|San Jose	|0.12		|3001		|Brad Guzan	    |London		|	    |5005|
___
19. Write a SQL statement to make a cartesian product between salesman and customer i.e. each salesman will appear for all customer and vice versa for those salesmen who belongs to a city and the customers who must have a grade.  

    ![Imgur](https://i.imgur.com/1zyR5od.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT *   
        FROM salesman a   
        CROSS JOIN  customer b   
        WHERE a.city IS NOT NULL   
        AND b.grade IS NOT NULL;

    |salesman_id	|name		|city	    |commission	|customer_id	|cust_name	    |city		|grade	|salesman_id|
    |---|---|---|---|---|---|---|---|---|
    |5001		|James Hoog	|New York	|0.15	    |3002		|Nick Rimando	|New York	|100	    |5001|
    |5002		|Nail Knite	|Paris		|0.13	    |3002		|Nick Rimando	|New York	|100	    |5001|
    |5005		|Pit Alex	|London		|0.11	    |3002		|Nick Rimando	|New York	|100	    |5001|
    |5006		|Mc Lyon		|Paris		|0.14	    |3002		|Nick Rimando	|New York	|100	    |5001|
    |5007		|Paul Adam	|Rome		|0.13	    |3002		|Nick Rimando	|New York	|100	    |5001|
    |5003		|Lauson Hen	|San Jose	|0.12	    |3002		|Nick Rimando	|New York	|100	    |5001|
    |5001		|James Hoog	|New York	|0.15	    |3007		|Brad Davis	    |New York	|200	    |5001|
    |5002		|Nail Knite	|Paris		|0.13	    |3007		|Brad Davis	    |New York	|200	    |5001|
    |5005		|Pit Alex	|London		|0.11	    |3007		|Brad Davis	    |New York	|200	    |5001|
    |5006		|Mc Lyon		|Paris		|0.14	    |3007		|Brad Davis	    |New York	|200	    |5001|
    |5007		|Paul Adam	|Rome		|0.13	    |3007		|Brad Davis	    |New York	|200	    |5001|
    |5003		|Lauson Hen	|San Jose	|0.12	    |3007		|Brad Davis	    |New York	|200	    |5001|
    |5001		|James Hoog	|New York	|0.15	    |3005		|Graham Zusi	    |California	|200	    |5002|
    |5002		|Nail Knite	|Paris		|0.13	    |3005		|Graham Zusi	    |California	|200	    |5002|
    |5005		|Pit Alex	|London		|0.11	    |3005		|Graham Zusi	    |California	|200	    |5002|
    |5006		|Mc Lyon		|Paris		|0.14	    |3005		|Graham Zusi	    |California	|200	    |5002|
    |5007		|Paul Adam	|Rome		|0.13	    |3005		|Graham Zusi	    |California	|200	    |5002|
    |5003		|Lauson Hen	|San Jose	|0.12	    |3005		|Graham Zusi	    |California	|200	    |5002|
    |5001		|James Hoog	|New York	|0.15	    |3008		|Julian Green	|London		|300	    |5002|
    |5002		|Nail Knite	|Paris		|0.13	    |3008		|Julian Green	|London		|300	    |5002|
    |5005		|Pit Alex	|London		|0.11	    |3008		|Julian Green	|London		|300	    |5002|
    |5006		|Mc Lyon		|Paris		|0.14	    |3008		|Julian Green	|London		|300	    |5002|
    |5007		|Paul Adam	|Rome		|0.13	    |3008		|Julian Green	|London		|300	    |5002|
    |5003		|Lauson Hen	|San Jose	|0.12	    |3008		|Julian Green	|London		|300	    |5002|
    |5001		|James Hoog	|New York	|0.15	    |3004		|Fabian Johnson	|Paris		|300	    |5006|
    |5002		|Nail Knite	|Paris		|0.13	    |3004		|Fabian Johnson	|Paris		|300	    |5006|
    |5005		|Pit Alex	|London		|0.11	    |3004		|Fabian Johnson	|Paris		|300	    |5006|
    |5006		|Mc Lyon		|Paris		|0.14	    |3004		|Fabian Johnson	|Paris		|300	    |5006|
    |5007		|Paul Adam	|Rome		|0.13	    |3004		|Fabian Johnson	|Paris		|300	    |5006|
    |5003		|Lauson Hen	|San Jose	|0.12	    |3004		|Fabian Johnson	|Paris		|300	    |5006|
    |5001		|James Hoog	|New York	|0.15	    |3009		|Geoff Cameron	|Berlin		|100	    |5003|
    |5002		|Nail Knite	|Paris		|0.13	    |3009		|Geoff Cameron	|Berlin		|100	    |5003|
    |5005		|Pit Alex	|London		|0.11	    |3009		|Geoff Cameron	|Berlin		|100	    |5003|
    |5006		|Mc Lyon		|Paris		|0.14	    |3009		|Geoff Cameron	|Berlin		|100	    |5003|
    |5007		|Paul Adam	|Rome		|0.13	    |3009		|Geoff Cameron	|Berlin		|100	    |5003|
    |5003		|Lauson Hen	|San Jose	|0.12	    |3009		|Geoff Cameron	|Berlin		|100	    |5003|
    |5001		|James Hoog	|New York	|0.15	    |3003		|Jozy Altidor	|Moscow		|200	    |5007|
    |5002		|Nail Knite	|Paris		|0.13	    |3003		|Jozy Altidor	|Moscow		|200	    |5007|
    |5005		|Pit Alex	|London		|0.11	    |3003		|Jozy Altidor	|Moscow		|200	    |5007|
    |5006		|Mc Lyon		|Paris		|0.14	    |3003		|Jozy Altidor	|Moscow		|200	    |5007|
    |5007		|Paul Adam	|Rome		|0.13	    |3003		|Jozy Altidor	|Moscow		|200	    |5007|
    |5003		|Lauson Hen	|San Jose	|0.12	    |3003		|Jozy Altidor	|Moscow		|200	    |5007|

___
20. Write a SQL statement to make a cartesian product between salesman and customer i.e. each salesman will appear for all customer and vice versa for those salesmen who must belong a city which is not the same as his customer and the customers should have an own grade.  

    ![Imgur](https://i.imgur.com/CWBmP4t.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT *   
        FROM salesman a   
        CROSS JOIN customer b   
        WHERE a.city IS NOT NULL   
        AND b.grade IS NOT NULL   
        AND  a.city<>b.city;

    |salesman_id	|name		|city	|commission	|customer_id	|cust_name	    |city		|grade	|salesman_id|
    |---|---|---|---|---|---|---|---|---|
    |5002		|Nail Knite	|Paris	|0.13		|3002		|Nick Rimando	|New York	|100	    |5001|
    |5005		|Pit Alex	|London	|0.11		|3002		|Nick Rimando	|New York	|100	    |5001|
    |5006		|Mc Lyon		|Paris	|0.14		|3002		|Nick Rimando	|New York	|100	    |5001|
    |5007		|Paul Adam	|Rome	|0.13		|3002		|Nick Rimando	|New York	|100	    |5001|
    |5003		|Lauson Hen	|San Jose|0.12		|3002		|Nick Rimando	|New York	|100	    |5001|
    |5002		|Nail Knite	|Paris	|0.13		|3007		|Brad Davis	    |New York	|200	    |5001|
    |5005		|Pit Alex	|London	|0.11		|3007		|Brad Davis	    |New York	|200	    |5001|
    |5006		|Mc Lyon		|Paris	|0.14		|3007		|Brad Davis	    |New York	|200	    |5001|
    |5007		|Paul Adam	|Rome	|0.13		|3007		|Brad Davis	    |New York	|200	    |5001|
    |5003		|Lauson Hen	|San Jose|0.12		|3007		|Brad Davis	    |New York	|200	    |5001|
    |5001		|James Hoog	|New York|0.15		|3005		|Graham Zusi	    |California	|200	    |5002|
    |5002		|Nail Knite	|Paris	|0.13		|3005		|Graham Zusi	    |California	|200	    |5002|
    |5005		|Pit Alex	|London	|0.11		|3005		|Graham Zusi	    |California	|200	    |5002|
    |5006		|Mc Lyon		|Paris	|0.14		|3005		|Graham Zusi	    |California	|200	    |5002|
    |5007		|Paul Adam	|Rome	|0.13		|3005		|Graham Zusi	    |California	|200	    |5002|
    |5003		|Lauson Hen	|San Jose|0.12		|3005		|Graham Zusi	    |California	|200	    |5002|
    |5001		|James Hoog	|New York|0.15		|3008		|Julian Green	|London		|300	    |5002|
    |5002		|Nail Knite	|Paris	|0.13		|3008		|Julian Green	|London		|300	    |5002|
    |5006		|Mc Lyon		|Paris	|0.14		|3008		|Julian Green	|London		|300	    |5002|
    |5007		|Paul Adam	|Rome	|0.13		|3008		|Julian Green	|London		|300	    |5002|
    |5003		|Lauson Hen	|San Jose|0.12		|3008		|Julian Green	|London		|300	    |5002|
    |5001		|James Hoog	|New York|0.15		|3004		|Fabian Johnson	|Paris		|300	    |5006|
    |5005		|Pit Alex	|London	|0.11		|3004		|Fabian Johnson	|Paris		|300	    |5006|
    |5007		|Paul Adam	|Rome	|0.13		|3004		|Fabian Johnson	|Paris		|300	    |5006|
    |5003		|Lauson Hen	|San Jose|0.12		|3004		|Fabian Johnson	|Paris		|300	    |5006|
    |5001		|James Hoog	|New York|0.15		|3009		|Geoff Cameron	|Berlin		|100	    |5003|
    |5002		|Nail Knite	|Paris	|0.13		|3009		|Geoff Cameron	|Berlin		|100	    |5003|
    |5005		|Pit Alex	|London	|0.11		|3009		|Geoff Cameron	|Berlin		|100	    |5003|
    |5006		|Mc Lyon		|Paris	|0.14		|3009		|Geoff Cameron	|Berlin		|100	    |5003|
    |5007		|Paul Adam	|Rome	|0.13		|3009		|Geoff Cameron	|Berlin		|100	    |5003|
    |5003		|Lauson Hen	|San Jose|0.12		|3009		|Geoff Cameron	|Berlin		|100	    |5003|
    |5001		|James Hoog	|New York|0.15		|3003		|Jozy Altidor	|Moscow		|200	    |5007|
    |5002		|Nail Knite	|Paris	|0.13		|3003		|Jozy Altidor	|Moscow		|200	    |5007|
    |5005		|Pit Alex	|London	|0.11		|3003		|Jozy Altidor	|Moscow		|200	    |5007|
    |5006		|Mc Lyon		|Paris	|0.14		|3003		|Jozy Altidor	|Moscow		|200	    |5007|
    |5007		|Paul Adam	|Rome	|0.13		|3003		|Jozy Altidor	|Moscow		|200	    |5007|
    |5003		|Lauson Hen	|San Jose|0.12		|3003		|Jozy Altidor	|Moscow		|200	    |5007|

___
21. Write a SQL query to display all the data from the item_mast, including all the data for each item's producer company. 

    ![Imgur](https://i.imgur.com/iDNJ1o0.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT *  
        FROM item_mast   
        INNER JOIN company_mast  
        ON item_mast.pro_com= company_mast.com_id; 

    |pro_id	|pro_name		|pro_price	|pro_com	|com_id	|com_name|
    |---|---|---|---|---|---|
    |101	|Mother Board		|3200.00		|15	    |15	    |Asus|
    |102	|Key Board		    |450.00		|16	    |16	    |Frontech|
    |103	|ZIP drive		    |250.00		|14	    |14	    |Zebronics|
    |104	|Speaker			    |550.00		|16	    |16	    |Frontech|
    |105	|Monitor			    |5000.00		|11	    |11	    |Samsung|
    |106	|DVD drive		    |900.00		|12	    |12	    |iBall|
    |107	|CD drive		    |800.00		|12	    |12	    |iBall|
    |108	|Printer			    |2600.00		|13	    |13	    |Epsion|
    |109	|Refill cartridge    |350.00		|13	    |13	    |Epsion|
    |110	|Mouse			    |250.00		|12	    |12	    |iBall|

___
22. Write a SQL query to display the item name, price, and company name of all the products.  

    ![Imgur](https://i.imgur.com/GnViDpv.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT item_mast.pro_name, pro_price, company_mast.com_name  
        FROM item_mast   
        INNER JOIN company_mast  
        ON item_mast.pro_com = company_mast.com_id; 

    |pro_name		|pro_price	|com_name|
    |---|---|---|
    |Mother Board	|3200.00		|Asus|
    |Key Board		|450.00		|Frontech|
    |ZIP drive		|250.00		|Zebronics|
    |Speaker			|550.00		|Frontech|
    |Monitor			|5000.00		|Samsung|
    |DVD drive		|900.00		|iBall|
    |CD drive		|800.00		|iBall|
    |Printer			|2600.00		|Epsion|
    |Refill cartridge|350.00		|Epsion||
    |Mouse			|250.00		|iBall|

___
23. Write a SQL query to display the average price of items of each company, showing the name of the company.  

    ![Imgur](https://i.imgur.com/ZnTU9wc.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT AVG(pro_price), company_mast.com_name  
        FROM item_mast INNER   
        JOIN company_mast  
        ON item_mast.pro_com= company_mast.com_id  
        GROUP BY company_mast.com_name;   

    |avg			            |com_name|
    |---|---|
    |5000.0000000000000000	|Samsung|
    |650.0000000000000000	|iBall|
    |1475.0000000000000000	|Epsion|
    |500.0000000000000000	|Frontech|
    |250.0000000000000000	|Zebronics|
    |3200.0000000000000000	|Asus|

___
24. Write a SQL query to display the names of the company whose products have an average price larger than or equal to Rs. 350.  

    ![Imgur](https://i.imgur.com/ytX7WsK.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT AVG(pro_price), company_mast.com_name  
        FROM item_mast   
        INNER JOIN company_mast  
        ON item_mast.pro_com = company_mast.com_id  
        GROUP BY company_mast.com_name  
        HAVING AVG(pro_price) >= 350;

    |avg	                    |com_name|
    |---|---|
    |5000.0000000000000000	|Samsung|
    |500.0000000000000000	|Frontech|
    |1475.0000000000000000	|Epsion|
    |650.0000000000000000	|iBall|
    |3200.0000000000000000	|Asus|

___
25. Write a SQL query to display the name of each company along with the ID and price for their most expensive product.  

    ![Imgur](https://i.imgur.com/00S3Rst.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT A.pro_name, A.pro_price, F.com_name  
        FROM item_mast A   
        INNER JOIN company_mast F  
        ON A.pro_com = F.com_id  
        AND A.pro_price =  
            (  
        SELECT MAX(A.pro_price)
            FROM item_mast A
            WHERE A.pro_com = F.com_id
        );

    |pro_name	|pro_price	|com_name|
    |---|---|---|
    |Monitor		|5000.00		|Samsung|
    |DVD drive	|900.00		|iBall|
    |Printer		|2600.00		|Epsion|
    |ZIP drive	|250.00		|Zebronics|
    |Mother Board|3200.00		|Asus|
    |Speaker		|550.00		|Frontech|

___
26. Write a query in SQL to display all the data of employees including their department.  

    ![Imgur](https://i.imgur.com/WBuvIrm.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT emp_idno, A.emp_fname AS "First Name",     
               emp_lname AS "Last Name",B.dpt_name AS "Department",   
               emp_dept, dpt_code,  dpt_allotment  
        FROM emp_details A   
        INNER JOIN emp_department B  
              ON A.emp_dept = B.dpt_code;  

    |emp_idno	|First Name	|Last Name	|Department	|emp_dept	|dpt_code	dpt_allotment|
    |---|---|---|---|---|---|---|
    |631548		|Alan		|Snappy		|RD		    |27		    |27		    55000|
    |839139		|Maria		|Foster		|IT		    |57		    |57		    65000|
    |127323		|Michale		|Robbin		|IT		    |57		    |57		    65000|
    |526689		|Carlos		|Snares		|Finance	    |63		    |63		    15000|
    |843795		|Enric		|Dosio		|IT		    |57		    |57		    65000|
    |328717		|Jhon		|Snares		|Finance	    |63		    |63		    15000|
    |444527		|Joseph		|Dosni		|HR		    |47		    |47		    240000|
    |659831		|Zanifer		|Emily		|HR		    |47		    |47		    240000|
    |847674		|Kuleswar	|Sitaraman	|IT		    |57		    |57		    65000|
    |748681		|Henrey		|Gabriel		|HR		    |47		    |47		    240000|
    |555935		|Alex		|Manuel		|IT		    |57		    |57		    65000|
    |539569		|George		|Mardy		|RD		    |27		    |27		    55000|
    |733843		|Mario		|Saule		|Finance		|63		    |63		    15000|
___
27. Write a query in SQL to display the first name and last name of each employee, along with the name and sanction amount for their department.  

    ![Imgur](https://i.imgur.com/d2Z0hzo.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT emp_details.emp_fname AS "First Name", emp_lname AS "Last Name", 
        emp_department.dpt_name AS "Department", 
        dpt_allotment AS "Amount Allotted"
        FROM emp_details 
            INNER JOIN emp_department
            ON emp_details.emp_dept = emp_department.dpt_code;
    
    |First Name	|Last Name	|Department	|Amount Allotted|
    |---|---|---|---|
    |Alan		|Snappy		|RD		    |55000|
    |Maria		|Foster		|IT		    |65000|
    |Michale		|Robbin		|IT		    |65000|
    |Carlos		|Snares		|Finance	    |15000|
    |Enric		|Dosio		|IT		    |65000|
    |Jhon		|Snares		|Finance	    |15000|
    |Joseph		|Dosni		|HR		    |240000|
    |Zanifer		|Emily		|HR		    |240000|
    |Kuleswar	|Sitaraman	|IT		    |65000|
    |Henrey		|Gabriel		|HR		    |240000|
    |Alex		|Manuel		|IT		    |65000|
    |George		|Mardy		|RD		    |55000|
    |Mario		|Saule		|Finance		|15000|

___
28. Write a query in SQL to find the first name and last name of employees working for departments with a budget more than Rs. 50000.  

    ![Imgur](https://i.imgur.com/F0xVoxC.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT emp_details.emp_fname AS "First Name",
        emp_lname AS "Last Name"
        FROM emp_details 
        INNER JOIN emp_department
              ON emp_details.emp_dept = emp_department.dpt_code
        AND emp_department.dpt_allotment > 50000;

    |First Name	|Last Name|
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


29. Write a query in SQL to find the names of departments where more than two employees are working.  

    ![Imgur](https://i.imgur.com/gAamxwO.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT emp_department.dpt_name
        FROM emp_details 
        INNER JOIN emp_department
        ON emp_dept =dpt_code
            GROUP BY emp_department.dpt_name
            HAVING COUNT(*) > 2;

    |dpt_name|
    |---|
    |Finance|
    |HR|
    |IT|
___