# SQL Exercises
## Using Boolean and Relational operators
![Imgur](https://i.imgur.com/vFHJMM1.png)
>SELECT * FROM customer WHERE grade > 100;
![Imgur](https://i.imgur.com/nCH6AHO.png)
___
![Imgur](https://i.imgur.com/pcTsEJZ.png)
>SELECT * FROM customer WHERE city = 'New York' AND grade>100;
![Imgur](https://i.imgur.com/Dcg9Q1V.png)
___
![Imgur](https://i.imgur.com/2gRZJNY.png)
>SELECT * FROM customer WHERE city = 'New York' OR grade>100;
![Imgur](https://i.imgur.com/gi78Ut2.png)
___
![Imgur](https://i.imgur.com/LJPzvSp.png)
>SELECT * FROM customer WHERE city = 'New York' OR NOT grade>100;
![Imgur](https://i.imgur.com/UHSxR7k.png)
___
![Imgur](https://i.imgur.com/Qa2GPQa.png)
>SELECT * FROM customer WHERE NOT (city = 'New York' OR grade>100);
![Imgur](https://i.imgur.com/66FQv6Y.png)
___
![Imgur](https://i.imgur.com/RMvw1e7.png)
>SELECT * FROM  orders WHERE NOT ((ord_date ='2012-09-10'AND salesman_id > 5005) OR purch_amt > 1000.00);
![Imgur](https://i.imgur.com/jP0RKxJ.png)
___
![Imgur](https://i.imgur.com/EyBXQSU.png)
>SELECT salesman_id,name,city,commission FROM salesman WHERE (commission > 0.10 AND commission< 0.12);
![Imgur](https://i.imgur.com/FVOcSLB.png)
___
![Imgur](https://i.imgur.com/jsrtZZ1.png)
>SELECT * FROM  orders WHERE(purch_amt<200 OR NOT(ord_date>='2012-02-10' AND customer_id<3009));
![Imgur](https://i.imgur.com/Mr9M96V.png)
___
![Imgur](https://i.imgur.com/ZRgWCVl.png)
>SELECT * FROM  orders WHERE NOT((ord_date ='2012-08-17' OR customer_id>3005) AND purch_amt<1000);
![Imgur](https://i.imgur.com/eIQeKZa.png)

___
![Imgur](https://i.imgur.com/VCnoCaQ.png)
>SELECT ord_no,purch_amt, (100*purch_amt)/6000 AS "Achieved %", (100*(6000-purch_amt)/6000) AS "Unachieved %" FROM  orders WHERE (100*purch_amt)/6000>50;
![Imgur](https://i.imgur.com/qRBgRes.png)

___
![Imgur](https://i.imgur.com/v8d994f.png)

>SELECT *  FROM emp_details  WHERE emp_lname ='Dosni' OR emp_lname= 'Mardy';
![Imgur](https://i.imgur.com/3q3xy8H.png)

___
![Imgur](https://i.imgur.com/jPTfCYq.png)
>SELECT *  FROM emp_details WHERE emp_dept = 47 OR emp_dept = 63;
![Imgur](https://i.imgur.com/BvhK1mw.png)

___
## Wildcard and Special operators
![Imgur](https://i.imgur.com/PsFgi5E.png)
>SELECT * FROM salesman WHERE city = 'Paris' OR city = 'Rome';
![Imgur](https://i.imgur.com/Jn16PP6.png)
___
![Imgur](https://i.imgur.com/DmIrI6v.png)
>SELECT * FROM salesman WHERE city IN('Paris','Rome');
![Imgur](https://i.imgur.com/iItoC2j.png)
___
![Imgur](https://i.imgur.com/vEqNm0x.png)
>SELECT * FROM salesman WHERE NOT city IN('Paris','Rome');
![Imgur](https://i.imgur.com/FELlQsE.png)
___
![Imgur](https://i.imgur.com/5zIoK4A.png)
>SELECT * 
FROM customer 
WHERE customer_id IN (3007,3008,3009);
![Imgur](https://i.imgur.com/OTgKHNZ.png)

___
![Imgur](https://i.imgur.com/0hFNJnw.png)
>SELECT * FROM salesman WHERE commission BETWEEN 0.12 AND 0.14;
![Imgur](https://i.imgur.com/IEnASH6.png)
___
![Imgur](https://i.imgur.com/q7bkdve.png)
>SELECT * FROM orders WHERE (purch_amt BETWEEN 500 AND 4000) AND NOT purch_amt IN(948.50,1983.43);
![Imgur](https://i.imgur.com/1tOWifE.png)

___
![Imgur](https://i.imgur.com/yV4jLAC.png)
>SELECT * FROM salesman WHERE name BETWEEN 'A' and 'L';
![Imgur](https://i.imgur.com/nLzArBg.png)
___
![Imgur](https://i.imgur.com/piZtsAH.png)
>SELECT * FROM salesman WHERE name NOT BETWEEN 'A' and 'L';
![Imgur](https://i.imgur.com/w8eqKdS.png)
___
![Imgur](https://i.imgur.com/cr6jQNb.png)
>SELECT * FROM customer WHERE cust_name LIKE 'B%';
![Imgur](https://i.imgur.com/QWZn6kZ.png)
___
![Imgur](https://i.imgur.com/yAeiZch.png)
>SELECT * FROM customer WHERE cust_name LIKE '%n';
![Imgur](https://i.imgur.com/Hebb0KT.png)
___
![Imgur](https://i.imgur.com/R5O5rFp.png)
>SELECT * FROM salesman WHERE name LIKE 'N__l%';
![Imgur](https://i.imgur.com/su6Ywdu.png)
___
![Imgur](https://i.imgur.com/hmf4lkt.png)
>SELECT * FROM testtable WHERE col1 LIKE '%/_%' ESCAPE '/';
![Imgur](https://i.imgur.com/3JjCnPL.png)
___
![Imgur](https://i.imgur.com/nH5UyZF.png)
>SELECT * FROM testtable WHERE col1 NOT LIKE '%/_%' ESCAPE '/';
![Imgur](https://i.imgur.com/nQb8rXa.png)
___
![Imgur](https://i.imgur.com/eDo5Cbf.png)
>SELECT * FROM testtable WHERE col1 LIKE '%//%' ESCAPE '/';
![Imgur](https://i.imgur.com/PYGJaQy.png)
___
![Imgur](https://i.imgur.com/vmb0GpI.png)
>SELECT * FROM testtable WHERE col1 NOT LIKE '%//%' ESCAPE '/';
![Imgur](https://i.imgur.com/fYmQZiZ.png)
___
![Imgur](https://i.imgur.com/oHHfDQi.png)
>SELECT * FROM testtable WHERE col1 LIKE '%/_//%' ESCAPE '/';
![Imgur](https://i.imgur.com/rukD8Pa.png)
___
![Imgur](https://i.imgur.com/ry1C4E0.png)
>SELECT * FROM testtable WHERE col1 NOT LIKE '%/_//%' ESCAPE '/';
![Imgur](https://i.imgur.com/LzUXOxM.png)
___
![Imgur](https://i.imgur.com/6EPGpY2.png)
>SELECT * FROM testtable WHERE col1 LIKE '%/%%' ESCAPE'/';
![Imgur](https://i.imgur.com/pF9XXUh.png)
___
![Imgur](https://i.imgur.com/PnUxpBq.png)
>SELECT * FROM testtable WHERE col1 NOT LIKE '%/%%' ESCAPE'/';
![Imgur](https://i.imgur.com/r6ziB4a.png)
___
![Imgur](https://i.imgur.com/zhlkTeI.png)
>SELECT * FROM customer WHERE grade IS NULL;
![Imgur](https://i.imgur.com/X8EU062.png)
___
![Imgur](https://i.imgur.com/6xYvbnk.png)
>SELECT * FROM customer WHERE NOT grade IS NULL;
![Imgur](https://i.imgur.com/7XKbqnU.png)
___
![Imgur](https://i.imgur.com/HBLxDC5.png)
>SELECT * FROM emp_details WHERE emp_lname LIKE 'D%';
![Imgur](https://i.imgur.com/9AerEPH.png)
___
## Aggregate Functions
![Imgur](https://i.imgur.com/iqJYb0j.png)
>SELECT SUM (purch_amt) FROM orders

| sum |
| --- |
| 17541.18 |

___
![Imgur](https://i.imgur.com/Rh7FluA.png)
>SELECT AVG (purch_amt) FROM orders

| avg |
| --- |
| 1461.7650000000000000 |
___
![Imgur](https://i.imgur.com/dfe3hES.png)
>SELECT COUNT (DISTINCT salesman_id) FROM orders

| count |
| --- |
| 6 |
___
![Imgur](https://i.imgur.com/mCTf6ou.png)
>SELECT COUNT(*) FROM customer;

| count |
| --- |
| 8 |
___
![Imgur](https://i.imgur.com/NpbDSlM.png)
>SELECT COUNT (ALL grade) FROM customer;

| count |
| --- |
| 7 |
___
![Imgur](https://i.imgur.com/sNpb2vU.png)
>SELECT MAX (purch_amt) FROM orders

| max |
| --- |
| 5760.00 |
___
![Imgur](https://i.imgur.com/z3TtqRY.png)
>SELECT MIN(purch_amt) FROM orders

| min |
| --- |
| 65.26 |
___
![Imgur](https://i.imgur.com/zPycVdY.png)
>SELECT city,MAX(grade) FROM customer GROUP BY city;

|city|	max|
|---|---|
|Moscow|	200|
|Paris	|300|
|London	|300|
|Berlin	|100|
|New York|	200|
|California|	200|

___
![Imgur](https://i.imgur.com/f9dSqyx.png)
>SELECT customer_id,MAX(purch_amt) FROM orders GROUP BY customer_id;

|customer_id	|max|
|---|---|
|3004	|1983.43|
|3007	|2400.60|
|3008	|250.45|
|3003	|75.29|
|3009	|2480.40|
|3002	|5760.00|
|3005	|948.50|
|3001	|270.65|
___
![Imgur](https://i.imgur.com/gO0zH9V.png)
>SELECT customer_id,ord_date,MAX(purch_amt) FROM orders GROUP BY customer_id,ord_date;
![Imgur](https://i.imgur.com/PH3s0ri.png)

___
![Imgur](https://i.imgur.com/dDw63E7.png)
>SELECT salesman_id,MAX(purch_amt) FROM orders WHERE ord_date = '2012-08-17' GROUP BY salesman_id;

|salesman_id|	max|
|---|---|
|5003	|110.50|
|5007	|75.29|
___
![Imgur](https://i.imgur.com/nd0AXvw.png)
>SELECT customer_id,ord_date,MAX(purch_amt) FROM orders GROUP BY customer_id,ord_date HAVING MAX(purch_amt)>2000.00;

|customer_id|	ord_date	|max|
|---|---|---|
|3007|	2012-07-27|	2400.60|
|3009|	2012-10-10|	2480.40|
|3002|	2012-09-10|	5760.00|
|3002|	2012-04-25|	3045.60|
___
![Imgur](https://i.imgur.com/f2YNsaZ.png)
>SELECT customer_id,ord_date,MAX(purch_amt) FROM orders GROUP BY customer_id,ord_date HAVING MAX(purch_amt) BETWEEN 2000 AND 6000;

|customer_id|	ord_date	|max|
|---|---|---|
|3007|	2012-07-27|	2400.60|
|3009|	2012-10-10|	2480.40|
|3002|	2012-09-10|	5760.00|
|3002|	2012-04-25|	3045.60|

___
![Imgur](https://i.imgur.com/ZeDpbaZ.png)
>SELECT customer_id,ord_date,MAX(purch_amt) FROM orders GROUP BY customer_id,ord_date HAVING MAX(purch_amt) IN(2000 ,3000,5760, 6000);

customer_id|	ord_date	|max|
|---|---|---|
|3002|	2012-09-10|	5760.00|

___
![Imgur](https://i.imgur.com/LjnUruY.png)
>SELECT customer_id,MAX(purch_amt) FROM orders WHERE customer_id BETWEEN 3002 and 3007 GROUP BY customer_id;

|customer_id|	max|
|---|---|
|3003|	75.29|
|3002|	5760.0|0
|3005|	948.50|
|3004|	1983.43|
|3007|	2400.60|
___
![Imgur](https://i.imgur.com/0ASSYwM.png)
>SELECT customer_id,MAX(purch_amt) FROM orders WHERE customer_id BETWEEN 3002 and 3007 GROUP BY customer_id HAVING MAX(purch_amt)>1000;

|customer_id|	max|
|---|---|
|3002|	5760.00|
|3004|	1983.43|
|3007|	2400.60|
___
![Imgur](https://i.imgur.com/1gRGq4P.png)
>SELECT salesman_id,MAX(purch_amt) FROM orders GROUP BY salesman_id HAVING salesman_id BETWEEN 5003 AND 5008;

|salesman_id|	max|
|---|---|
|5006|	1983.43|
|5003|	2480.40|
|5005|	270.65|
|5007|	75.29|
___
![Imgur](https://i.imgur.com/AnmJZ0U.png)
>SELECT COUNT(*) FROM orders WHERE ord_date='2012-08-17';

|count|
|---|
|2|
___
![Imgur](https://i.imgur.com/a234zev.png)
>SELECT COUNT(*) FROM salesman WHERE city IS NOT NULL;

|count|
|---|
|6|
___
![Imgur](https://i.imgur.com/yJE759Y.png)
>SELECT ord_date,salesman_id,COUNT(*) FROM orders GROUP BY ord_date,salesman_id;
![Imgur](https://i.imgur.com/aqb03IA.png)
___
![Imgur](https://i.imgur.com/7e5aJxd.png)
>SELECT AVG(pro_price) AS "Average Price" FROM item_mast;

|Average Price|
|---|
|1435.0000000000000000|
___
![Imgur](https://i.imgur.com/S8AxTxs.png)
>SELECT COUNT(*) AS "Number of Products" 
  FROM item_mast 
    WHERE pro_price >= 350;

|Number of Products|
|---|
|8|
___
![Imgur](https://i.imgur.com/fKAOOGd.png)
>SELECT AVG(pro_price) AS "Average Price", pro_com AS "Company ID" FROM item_mast GROUP BY pro_com;

|Average Price|	Company ID|
|---|---|
|5000.0000000000000000|	11|
|1475.0000000000000000|	13|
|500.0000000000000000|	16|
|3200.0000000000000000|	15|
|650.0000000000000000	|12|
|250.0000000000000000	|14|
___
![Imgur](https://i.imgur.com/vzk9XiE.png)
>SELECT SUM(dpt_allotment) FROM emp_department;

|sum|
|---|
|450000|
___
![Imgur](https://i.imgur.com/P3wL5Fj.png)
>SELECT emp_dept, COUNT(*) FROM emp_details GROUP BY emp_dept;

|emp_dept|	count|
|---|---|
|47|	3|
|27|	2|
|63	|3|
|57|	5|
___
## Formatting Query Output
![Imgur](https://i.imgur.com/VG41y8X.png)
>SELECT salesman_id,name,city,'%',commission*100 FROM salesman;

|salesman_id|	name|	city|	?column?|
|---|---|---|---|
|5001	|James Hoog|	New York|	15.00|
|5002	|Nail Knite	|Paris	|13.00|
|5005	|Pit Alex	|London|	11.00|
|5006	|Mc Lyon|	Paris	|14.00|
|5007	|Paul Adam|	Rome	|13.00|
|5003	|Lauson Hen	|San Jose|	12.00|
___
![Imgur](https://i.imgur.com/QfIKdW7.png)
>SELECT ' For',ord_date,',there are', COUNT (DISTINCT ord_no),'orders.' FROM orders GROUP BY ord_date;
![Imgur](https://i.imgur.com/Izf52MS.png)
___
![Imgur](https://i.imgur.com/1yqDbY6.png)
>SELECT * FROM orders ORDER BY ord_no;
![Imgur](https://i.imgur.com/qoMBA2n.png)
___
![Imgur](https://i.imgur.com/Jdpaym2.png)
>SELECT * FROM orders ORDER BY ord_date DESC;
![Imgur](https://i.imgur.com/dJV144M.png)
___
![Imgur](https://i.imgur.com/zDGw4B2.png)
>SELECT * FROM orders ORDER BY ord_date,purch_amt DESC;
![Imgur](https://i.imgur.com/B9WGLBo.png)
___
![Imgur](https://i.imgur.com/fuOMiHn.png)
>SELECT cust_name,city,grade FROM customer ORDER BY customer_id;

>![Imgur](https://i.imgur.com/IyS3kow.png)
___
![Imgur](https://i.imgur.com/HU2yn8K.png)
>SELECT salesman_id,ord_date,MAX(purch_amt) FROM orders GROUP BY salesman_id,ord_date ORDER BY salesman_id,ord_date;

>![Imgur](https://i.imgur.com/MRuvWJM.png)
___
![Imgur](https://i.imgur.com/lfL5qzX.png)
>SELECT cust_name,city,grade FROM customer ORDER BY 3 DESC;
>![Imgur](https://i.imgur.com/VwVkXXH.png)
___
![Imgur](https://i.imgur.com/A58pvlR.png)
>SELECT customer_id, COUNT(DISTINCT ord_no), MAX(purch_amt) FROM orders GROUP BY customer_id ORDER BY 2 DESC;

>![Imgur](https://i.imgur.com/n0Ti9AA.png)
___
![Imgur](https://i.imgur.com/D2NRZBp.png)
>SELECT ord_date, SUM(purch_amt), SUM(purch_amt)*.15 FROM orders GROUP BY ord_date ORDER BY ord_date;

>![Imgur](https://i.imgur.com/qiJbfZ6.png)
___
## Query on Multiple Tables
![Imgur](https://i.imgur.com/kmgnsTT.png)
>SELECT customer.cust_name,salesman.name, salesman.city FROM salesman, customer WHERE salesman.city = customer.city;

>![Imgur](https://i.imgur.com/jFvKqX8.png)
___
![Imgur](https://i.imgur.com/o2TqF2V.png)
>SELECT customer.cust_name, salesman.name FROM customer,salesman WHERE salesman.salesman_id = customer.salesman_id;

>![Imgur](https://i.imgur.com/qWEaw2o.png)
___
![Imgur](https://i.imgur.com/I3bR6P4.png)
![Imgur](https://i.imgur.com/50OHx49.png)
>SELECT ord_no, cust_name, orders.customer_id, orders.salesman_id FROM salesman, customer, orders WHERE customer.city <> salesman.city AND orders.customer_id = customer.customer_id AND orders.salesman_id = salesman.salesman_id;

>![Imgur](https://i.imgur.com/j5eXzOl.png)
___
![Imgur](https://i.imgur.com/wPzGxPB.png)
>SELECT orders.ord_no, customer.cust_name FROM orders, customer WHERE orders.customer_id = customer.customer_id;

>![Imgur](https://i.imgur.com/5Hxohfn.png)
___
![Imgur](https://i.imgur.com/CZiWlYb.png)
![Imgur](https://i.imgur.com/GiAfR2H.png)
>SELECT customer.cust_name AS "Customer", customer.grade AS "Grade" FROM orders, salesman, customer WHERE orders.customer_id = customer.customer_id
AND orders.salesman_id = salesman.salesman_id AND salesman.city IS NOT NULL AND customer.grade IS NOT NULL;

>![Imgur](https://i.imgur.com/z2G9NvX.png)
___
![Imgur](https://i.imgur.com/GViFwcv.png)
>SELECT customer.cust_name AS "Customer", customer.city AS "City", salesman.name AS "Salesman", salesman.commission FROM customer,salesman
WHERE customer.salesman_id = salesman.salesman_id AND salesman.commission BETWEEN .12 AND .14;

>![Imgur](https://i.imgur.com/mGsjAzE.png)
___
![Imgur](https://i.imgur.com/InpyWxX.png)
![Imgur](https://i.imgur.com/VXiYu3r.png)
>SELECT ord_no, cust_name, commission AS "Commission%", purch_amt*commission AS "Commission" FROM salesman,orders,customer WHERE orders.customer_id = customer.customer_id AND orders.salesman_id = salesman.salesman_id AND customer.grade>=200;

>![Imgur](https://i.imgur.com/sL84eEX.png)
___
![Imgur](https://i.imgur.com/g03K5vq.png)
![Imgur](https://i.imgur.com/75Q38ei.png)
>SELECT *
FROM customer a,orders  b 
WHERE a.customer_id=b.customer_id 
AND b.ord_date='2012-10-05';

>![Imgur](https://i.imgur.com/8HTDool.png)
___
## SQL JOINS
1. Write a SQL statement to prepare a list with salesman name, customer name and their cities for the salesmen and customer who belongs to the same city.    

    ![Imgur](https://i.imgur.com/pv6oghU.png)
    >SELECT salesman.name AS "Salesman", customer.cust_name, customer.city FROM salesman,customer WHERE salesman.city=customer.city;

    >![Imgur](https://i.imgur.com/rlSzdEZ.png)
 
___
2. Write a SQL statement to make a list with order no, purchase amount, customer name and their cities for those orders which order amount between 500 and 2000.  

    ![Imgur](https://i.imgur.com/xsHwqmT.png)
    >SELECT a.ord_no,a.purch_amt, b.cust_name,b.city FROM orders a,customer b WHERE a.customer_id=b.customer_id AND a.purch_amt BETWEEN 500 AND 2000;

    |ord_no|	purch_amt|	cust_name|	city|
    |---|---|---|---|
    |70007|	948.50|	Graham Zusi|	California|
    |70010|	1983.43|	Fabian Johnson|	Paris|
___
3. Write a SQL statement to know which salesman are working for which customer.  

    ![Imgur](https://i.imgur.com/vKaPNRi.png)
    >SELECT a.cust_name AS "Customer Name", a.city, b.name AS "Salesman", b.commission FROM customer a INNER JOIN salesman b ON a.salesman_id=b.salesman_id;

    >![Imgur](https://i.imgur.com/C4wLiMj.png)
___
4. Write a SQL statement to find the list of customers who appointed a salesman for their jobs who gets a commission from the company is more than 12%.   

    ![Imgur](https://i.imgur.com/l3FojlZ.png)
    >SELECT a.cust_name AS "Customer Name", a.city, b.name AS "Salesman", b.commission FROM customer a INNER JOIN salesman b ON a.salesman_id=b.salesman_id WHERE b.commission>.12;

    >![Imgur](https://i.imgur.com/U5fXWD1.png)
___
5. Write a SQL statement to find the list of customers who appointed a salesman for their jobs who does not live in the same city where their customer lives, and gets a commission is above 12% .   

    ![Imgur](https://i.imgur.com/dxK6lUH.png)
    >SELECT a.cust_name AS "Customer Name", a.city, b.name AS "Salesman", b.city,b.commission FROM customer a INNER JOIN salesman b ON a.salesman_id=b.salesman_id WHERE b.commission>.12 AND a.city<>b.city;

    |Customer Name|	city|	Salesman|	commission|
    |---|---|---|---|
    |Graham Zusi|	Paris|	Nail Knite|	0.13|
    |Julian Green|	Paris|	Nail Knite|	0.13|
    |Jozy Altidor|	Rome|	Paul Adam|	0.13|
___
6. Write a SQL statement to find the details of a order i.e. order number, order date, amount of order, which customer gives the order and which salesman works for that customer and how much commission he gets for an order.   

    ![Imgur](https://i.imgur.com/vtMVDND.png)
    ![Imgur](https://i.imgur.com/4uYPvQU.png)
___
7. Write a SQL statement to make a join on the tables salesman, customer and orders in such a form that the same column of each table will appear once and only the relational rows will come.  

    ![Imgur](https://i.imgur.com/vr7Gzl4.png)
    ![Imgur](https://i.imgur.com/Xsf0V7j.png)
___
8. Write a SQL statement to make a list in ascending order for the customer who works either through a salesman or by own.   

    ![Imgur](https://i.imgur.com/ndf2rSo.png)
___
9. Write a SQL statement to make a list in ascending order for the customer who holds a grade less than 300 and works either through a salesman or by own. 

    ![Imgur](https://i.imgur.com/08Mw7xs.png)
___
10. Write a SQL statement to make a report with customer name, city, order number, order date, and order amount in ascending order according to the order date to find that either any of the existing customers have placed no order or placed one or more orders.  

    ![Imgur](https://i.imgur.com/fPb4nXm.png)
___
11. Write a SQL statement to make a report with customer name, city, order number, order date, order amount salesman name and commission to find that either any of the existing customers have placed no order or placed one or more orders by their salesman or by own.  

    ![Imgur](https://i.imgur.com/78nvvQX.png)
    ![Imgur](https://i.imgur.com/jqZ684Z.png)
___
12. Write a SQL statement to make a list in ascending order for the salesmen who works either for one or more customer or not yet join under any of the customers.  

    ![Imgur](https://i.imgur.com/7EwUN3Z.png)
___
13. Write a SQL statement to make a list for the salesmen who works either for one or more customer or not yet join under any of the customers who placed either one or more orders or no order to their supplier.  

    ![Imgur](https://i.imgur.com/zNvqJEr.png)
    ![Imgur](https://i.imgur.com/9jZNHF9.png)
___
14. Write a SQL statement to make a list for the salesmen who either work for one or more customers or yet to join any of the customer. The customer may have placed, either one or more orders on or above order amount 2000 and must have a grade, or he may not have placed any order to the associated supplier.  

    ![Imgur](https://i.imgur.com/SWqOL2j.png)
    ![Imgur](https://i.imgur.com/pDlRSju.png)
___
15. Write a SQL statement to make a report with customer name, city, order no. order date, purchase amount for those customers from the existing list who placed one or more orders or which order(s) have been placed by the customer who is not on the list.  

    ![Imgur](https://i.imgur.com/r1i0Q8U.png)
___
16. Write a SQL statement to make a report with customer name, city, order no. order date, purchase amount for only those customers on the list who must have a grade and placed one or more orders or which order(s) have been placed by the customer who is neither in the list not have a grade.  

    ![Imgur](https://i.imgur.com/06FXxxM.png)
___
17. Write a SQL statement to make a cartesian product between salesman and customer i.e. each salesman will appear for all customer and vice versa.  

    ![Imgur](https://i.imgur.com/4j9zhdK.png)
___
18. Write a SQL statement to make a cartesian product between salesman and customer i.e. each salesman will appear for all customer and vice versa for that salesman who belongs to a city.  

    ![Imgur](https://i.imgur.com/kkRwu8u.png)
___
19. Write a SQL statement to make a cartesian product between salesman and customer i.e. each salesman will appear for all customer and vice versa for those salesmen who belongs to a city and the customers who must have a grade.  

    ![Imgur](https://i.imgur.com/1zyR5od.png)
___
20. Write a SQL statement to make a cartesian product between salesman and customer i.e. each salesman will appear for all customer and vice versa for those salesmen who must belong a city which is not the same as his customer and the customers should have an own grade.  

    ![Imgur](https://i.imgur.com/CWBmP4t.png)
___
21. Write a SQL query to display all the data from the item_mast, including all the data for each item's producer company. 

    ![Imgur](https://i.imgur.com/iDNJ1o0.png)
___
22. Write a SQL query to display the item name, price, and company name of all the products.  

    ![Imgur](https://i.imgur.com/GnViDpv.png)
___
23. Write a SQL query to display the average price of items of each company, showing the name of the company.  

    ![Imgur](https://i.imgur.com/ZnTU9wc.png)
___
24. Write a SQL query to display the names of the company whose products have an average price larger than or equal to Rs. 350.  

    ![Imgur](https://i.imgur.com/ytX7WsK.png)
___
25. Write a SQL query to display the name of each company along with the ID and price for their most expensive product.  

    ![Imgur](https://i.imgur.com/00S3Rst.png)
___
26. Write a query in SQL to display all the data of employees including their department.  

    ![Imgur](https://i.imgur.com/WBuvIrm.png)
___
27. Write a query in SQL to display the first name and last name of each employee, along with the name and sanction amount for their department.  

    ![Imgur](https://i.imgur.com/d2Z0hzo.png)
___
28. Write a query in SQL to find the first name and last name of employees working for departments with a budget more than Rs. 50000.  

    ![Imgur](https://i.imgur.com/F0xVoxC.png)

29. Write a query in SQL to find the names of departments where more than two employees are working.  

    ![Imgur](https://i.imgur.com/gAamxwO.png)
___
## SUBQUERIES
1. Write a query to display all the orders from the orders table issued by the salesman 'Paul Adam'.  

    ![Imgur](https://i.imgur.com/KWGQj4l.png)
___
2. Write a query to display all the orders for the salesman who belongs to the city London.  

    ![Imgur](https://i.imgur.com/KWGQj4l.png)
___
3. Write a query to find all the orders issued against the salesman who may works for customer whose id is 3007.  

    ![Imgur](https://i.imgur.com/KWGQj4l.png)
___
4. Write a query to display all the orders which values are greater than the average order value for 10th October 2012.  

    ![Imgur](https://i.imgur.com/KWGQj4l.png)
___
5. Write a query to find all orders attributed to a salesman in New york.  

    ![Imgur](https://i.imgur.com/KWGQj4l.png)
___
6. Write a query to display the commission of all the salesmen servicing customers in Paris.  

    ![Imgur](https://i.imgur.com/cd0UQ1R.png)
___

7. Write a query to display all the customers whose id is 2001 bellow the salesman ID of Mc Lyon.  

    ![Imgur](https://i.imgur.com/cd0UQ1R.png)
___
 
8. Write a query to count the customers with grades above New York's average.  

    ![Imgur](https://i.imgur.com/xNTaFOq.png)
___
9. Write a query to extract the data from the orders table for those salesman who earned the maximum commission  

    ![Imgur](https://i.imgur.com/5josRY9.png)
    ![Imgur](https://i.imgur.com/6AtwDjj.png)
___

10. Write a query to display all the customers with orders issued on date 17th August, 2012.  

    ![Imgur](https://i.imgur.com/lXgme14.png)
___

11. Write a query to find the name and numbers of all salesmen who had more than one customer.  

    ![Imgur](https://i.imgur.com/GLOGcQK.png)
___

12. Write a query to find all orders with order amounts which are above-average amounts for their customers.  

    ![Imgur](https://i.imgur.com/u4S0LSc.png)
___

13. Write a queries to find all orders with order amounts which are on or above-average amounts for their customers.  

    ![Imgur](https://i.imgur.com/u4S0LSc.png)
___

14. Write a query to find the sums of the amounts from the orders table, grouped by date, eliminating all those dates where the sum was not at least 1000.00 above the maximum order amount for that date.  

    ![Imgur](https://i.imgur.com/u4S0LSc.png)
___
15. Write a query to extract the data from the customer table if and only if one or more of the customers in the customer table are located in London.  

    ![Imgur](https://i.imgur.com/wMGHFTQ.png)
___
16. Write a query to find the salesmen who have multiple customers. 

    ![Imgur](https://i.imgur.com/u4jFJwl.png)
___
17. Write a query to find all the salesmen who worked for only one customer.  

    ![Imgur](https://i.imgur.com/a6I2n6R.png)
___

18. Write a query that extract the rows of all salesmen who have customers with more than one orders.  

    ![Imgur](https://i.imgur.com/9xp9rHP.png)
    ![Imgur](https://i.imgur.com/OmAjQKY.png)
___

19. Write a query to find salesmen with all information who lives in the city where any of the customers lives. 

    ![Imgur](https://i.imgur.com/ma9l4Tn.png)
___

20. Write a query to find all the salesmen for whom there are customers that follow them. G

    ![Imgur](https://i.imgur.com/ma9l4Tn.png)
___

21. Write a query to display the salesmen which name are alphabetically lower than the name of the customers. 

    ![Imgur](https://i.imgur.com/ma9l4Tn.png)
___

22. Write a query to display the customers who have a greater gradation than any customer who belongs to the alphabetically lower than the city New York. 

    ![Imgur](https://i.imgur.com/ma9l4Tn.png)
___

23. Write a query to display all the orders that had amounts that were greater than at least one of the orders on September 10th 2012. 

    ![Imgur](https://i.imgur.com/sp8LUwS.png)
___

24. Write a query to find all orders with an amount smaller than any amount for a customer in London. (Using ANY keyword)  

    ![Imgur](https://i.imgur.com/FVl1755.png)
___

25. Write a query to display all orders with an amount smaller than any amount for a customer in London. (Using MAX) 

    ![Imgur](https://i.imgur.com/eM0VrmF.png)
___

26. Write a query to display only those customers whose grade are, in fact, higher than every customer in New York. 

    ![Imgur](https://i.imgur.com/RVr2gR9.png)
___

27. Write a query in sql to find the name, city, and the total sum of orders amount a salesman collects. Salesman should belong to the cities where any of the customer belongs. 

    ![Imgur](https://i.imgur.com/t77rP3h.png)
___

28. Write a query to get all the information for those customers whose grade is not as the grade of customer who belongs to the city London.  

    ![Imgur](https://i.imgur.com/PE13mHx.png)
___
29. Write a query to find all those customers whose grade are not as the grade, belongs to the city Paris. 

    ![Imgur](https://i.imgur.com/PE13mHx.png)
___

30. Write a query to find all those customers who hold a different grade than any customer of the city Dallas. 

    ![Imgur](https://i.imgur.com/PE13mHx.png)
___

31. Write a SQL query to find the average price of each manufacturer's products along with their name.

    ![Imgur](https://i.imgur.com/9M5rosR.png)
___

32. Write a SQL query to display the average price of the products which is more than or equal to 350 along with their names.

    ![Imgur](https://i.imgur.com/9M5rosR.png)
___

33. Write a SQL query to display the name of each company, price for their most expensive product along with their Name.


    ![Imgur](https://i.imgur.com/9M5rosR.png)
___

34. Write a query in SQL to find all the details of employees whose last name is Gabriel or Dosio.

    ![Imgur](https://i.imgur.com/97lHr4P.png)
___

35. Write a query in SQL to display all the details of employees who works in department 89 or 63.

    ![Imgur](https://i.imgur.com/ZacgzmS.png)
___

36. Write a query in SQL to display the first name and last name of employees working for the department which allotment amount is more than Rs.50000.

    ![Imgur](https://i.imgur.com/ZacgzmS.png)
___

37. Write a query in SQL to find the departments which sanction amount is larger than the average sanction amount of all the departments.


    ![Imgur](https://i.imgur.com/JUrsR2v.png)
___
38. Write a query in SQL to find the names of departments with more than two employees are working.


    ![Imgur](https://i.imgur.com/3v1R4sn.png)
___

39. Write a query in SQL to find the first name and last name of employees working for departments which sanction amount is second lowest.


    ![Imgur](https://i.imgur.com/3v1R4sn.png)
___

## FILTERING and SORTING on HR Database
1. Write a query in SQL to display the full name (first and last name), and salary for those employees who earn below 6000.  
>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___
2. Write a query in SQL to display the first and last_name, department number and salary for those employees who earn more than 8000.  
>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___
3. Write a query in SQL to display the first and last name, and department number for all employees whose last name is “McEwen”.  

>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___

4. Write a query in SQL to display all the information for all employees without any department number.  

>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___
5. Write a query in SQL to display all the information about the department Marketing.  

>Sample table: departments
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/pDBOoDN"><img src="https://i.imgur.com/pDBOoDN.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/dSNLw2C"><img src="https://i.imgur.com/dSNLw2C.png" title="source: imgur.com" /></a>
</div>

___
6. Write a query in SQL to display the full name (first and last), hire date, salary, and department number for those employees whose first name does not containing the letter M and make the result set in ascending order by department number.  

>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___
7. Write a query in SQL to display all the information of employees whose salary is in the range of 8000 and 12000 and commission is not null or department number is except the number 40, 120 and 70 and they have been hired before June 5th, 1987. 

>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___
8. Write a query in SQL to display the full name (first and last name), and salary for all employees who does not earn any commission.  

>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___
9. Write a query in SQL to display the full name (first and last), the phone number and email separated by hyphen, and salary, for those employees whose salary is within the range of 9000 and 17000. The column headings assign with Full_Name, Contact_Details and Remuneration respectively.  

>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___
10. Write a query in SQL to display the first and last name, and salary for those employees whose first name is ending with the letter m.  

>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___
11. Write a query in SQL to display the full name (first and last) name, and salary, for all employees whose salary is out of the range 7000 and 15000 and make the result set in ascending order by the full name.  
>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>
    
___
12. Write a query in SQL to display the full name (first and last), job id and date of hire for those employees who was hired during November 5th, 2007 and July 5th, 2009. 
>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___
13. Write a query in SQL to display the the full name (first and last name), and department number for those employees who works either in department 70 or 90.  

>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___
14. Write a query in SQL to display the full name (first and last name), salary, and manager number for those employees who is working under a manager.  

>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___
15. Write a query in SQL to display all the information from Employees table for those employees who was hired before June 21st, 2002.  

>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___
16. Write a query in SQL to display the first and last name, email, salary and manager ID, for those employees whose managers are hold the ID 120, 103 or 145.  

>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___
17. Write a query in SQL to display all the information for all employees who have the letters D, S, or N in their first name and also arrange the result in descending order by salary.  

>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___
18. Write a query in SQL to display the full name (first name and last name), hire date, commission percentage, email and telephone separated by '-', and salary for those employees who earn the salary above 11000 or the seventh digit in their phone number equals 3 and make the result set in a descending order by the first name.  

>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___
19. Write a query in SQL to display the first and last name, and department number for those employees who holds a letter s as a 3rd character in their first name. 

>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___
20. Write a query in SQL to display the employee ID, first name, job id, and department number for those employees who is working except the departments 50,30 and 80. 

>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___
21. Write a query in SQL to display the employee Id, first name, job id, and department number for those employees whose department number equals 30, 40 or 90.  

>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___
22. Write a query in SQL to display the ID for those employees who did two or more jobs in the past.  

>Sample table : job_history

![Imgur](https://i.imgur.com/QODF31m.png)

___
23. Write a query in SQL to display job ID, number of employees, sum of salary, and difference between highest salary and lowest salary for a job.  
>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___
24. Write a query in SQL to display job ID for those jobs that were done by two or more for more than 300 days.  

>Sample table : job_history

![Imgur](https://i.imgur.com/QODF31m.png)
___

25. Write a query in SQL to display the country ID and number of cities in that country we have.  

>Sample table : locations
<div style="overflow-x: scroll; max-width: 600px; height: 150px">
    <a href="https://imgur.com/a9rNy8j"><img src="https://i.imgur.com/a9rNy8j.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/5oDRNZO"><img src="https://i.imgur.com/5oDRNZO.png" title="source: imgur.com" /></a>
</div>

___
26. Write a query in SQL to display the manager ID and number of employees managed by the manager.  

>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___
27. Write a query in SQL to display the details of jobs in descending sequence on job title.  

>Sample table : jobs
<div style="overflow-x: scroll; max-width: 650px; height: 250px">
   <a href="https://imgur.com/zjzO4hG"><img src="https://i.imgur.com/zjzO4hG.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8nY18X4"><img src="https://i.imgur.com/8nY18X4.png" title="source: imgur.com" /></a>
</div>

___
28. Write a query in SQL to display the first and last name and date of joining of the employees who is either Sales Representative or Sales Man.  

>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___
29. Write a query in SQL to display the average salary of employees for each department who gets a commission percentage.  

>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___
30. Write a query in SQL to display those departments where any manager is managing 4 or more employees.  

>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___
31. Write a query in SQL to display those departments where more than ten employees work who got a commission percentage.  

>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___
32. Write a query in SQL to display the employee ID and the date on which he ended his previous job.  

>Sample table : job_history

![Imgur](https://i.imgur.com/QODF31m.png)
___

33. Write a query in SQL to display the details of the employees who have no commission percentage and salary within the range 7000 to 12000 and works in that department which number is 50.  

>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___
34. Write a query in SQL to display the job ID for those jobs which average salary is above 8000.  

>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___
35. Write a query in SQL to display job Title, the difference between minimum and maximum salaries for those jobs which max salary within the range 12000 to 18000.  

>Sample table : jobs
<div style="overflow-x: scroll; max-width: 650px; height: 250px">
   <a href="https://imgur.com/zjzO4hG"><img src="https://i.imgur.com/zjzO4hG.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8nY18X4"><img src="https://i.imgur.com/8nY18X4.png" title="source: imgur.com" /></a>
</div>

___
36. Write a query in SQL to display all those employees whose first name or last name starts with the letter D.  

>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___
37. Write a query in SQL to display the details of jobs which minimum salary is greater than 9000.  

>Sample table : jobs
<div style="overflow-x: scroll; max-width: 650px; height: 250px">
   <a href="https://imgur.com/zjzO4hG"><img src="https://i.imgur.com/zjzO4hG.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8nY18X4"><img src="https://i.imgur.com/8nY18X4.png" title="source: imgur.com" /></a>
</div>

___
38. Write a query in SQL to display those employees who joined after 7th September, 1987.  

>Sample table: employees
<div style="overflow-x: scroll; max-width: 750px; height: 250px">
    <a href="https://imgur.com/yvhvDGi"><img src="https://i.imgur.com/yvhvDGi.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/JpkMz0t"><img src="https://i.imgur.com/JpkMz0t.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/8bUml4Q"><img src="https://i.imgur.com/8bUml4Q.png" title="source: imgur.com" /></a>
    <a href="https://imgur.com/TzAm2Wb"><img src="https://i.imgur.com/TzAm2Wb.png" title="source: imgur.com" /></a>
   <a href="https://imgur.com/0apI3m4"><img src="https://i.imgur.com/0apI3m4.png" title="source: imgur.com" /></a>
</div>

___

<pre style="max-height: 80px; 
overflow-y: auto;  background-color: #FFFFCC;" >
<code> salesman_id |    name    |   city   | commission 
-------------+------------+----------+------------
        5001 | James Hoog | New York |       0.15
        5002 | Nail Knite | Paris    |       0.13
        5005 | Pit Alex   | London   |       0.11
        5006 | Mc Lyon    | Paris    |       0.14
        5007 | Paul Adam  | Rome     |       0.13
        5003 | Lauson Hen | San Jose |       0.12</code>
</pre>



