# SQL Exercises
## Query on Multiple Tables
![Imgur](https://i.imgur.com/kmgnsTT.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

SELECT customer.cust_name, salesman.name, salesman.city   
FROM salesman, customer   
WHERE salesman.city = customer.city;  

|cust_name	    |name		|city|
|---|---|---|
|Nick Rimando	|James Hoog	|New York|
|Brad Davis	    |James Hoog	|New York|
|Julian Green	|Pit Alex	|London|
|Fabian Johnson	|Mc Lyon		|Paris|
|Fabian Johnson	|Nail Knite	|Paris|
|Brad Guzan	    |Pit Alex	|London|
___
![Imgur](https://i.imgur.com/o2TqF2V.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

SELECT customer.cust_name, salesman.name   
FROM customer,salesman   
WHERE salesman.salesman_id = customer.salesman_id;  

|cust_name	    |name|
|---|---|
|Nick Rimando	|James Hoog|
|Brad Davis	    |James Hoog|
|Graham Zusi	    |Nail Knite|
|Julian Green	|Nail Knite|
|Fabian Johnson	|Mc Lyon|
|Geoff Cameron	|Lauson Hen|
|Jozy Altidor	|Paul Adam|
|Brad Guzan	    |Pit Alex|

___
![Imgur](https://i.imgur.com/I3bR6P4.png)
![Imgur](https://i.imgur.com/50OHx49.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

SELECT ord_no, cust_name, orders.customer_id, orders.salesman_id     
FROM salesman, customer, orders   
WHERE customer.city <> salesman.city   
AND orders.customer_id = customer.customer_id   
AND orders.salesman_id = salesman.salesman_id;  

|ord_no	|cust_name	    |customer_id	|salesman_id|
|---|---|---|---|
|70004	|Geoff Cameron	|3009		|5003|
|70003	|Geoff Cameron	|3009		|5003|
|70011	|Jozy Altidor	|3003		|5007|
|70001	|Graham Zusi	    |3005		|5002|
|70007	|Graham Zusi	    |3005		|5002|
|70012	|Julian Green	|3008		|5002|
___
![Imgur](https://i.imgur.com/wPzGxPB.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

SELECT orders.ord_no, customer.cust_name   
FROM orders, customer   
WHERE orders.customer_id = customer.customer_id;  

|ord_no	|cust_name|
|---|---|
|70009	|Brad Guzan|
|70002	|Nick Rimando|
|70004	|Geoff Cameron|
|70005	|Brad Davis|
|70008	|Nick Rimando|
|70010	|Fabian Johnson|
|70003	|Geoff Cameron|
|70011	|Jozy Altidor|
|70013	|Nick Rimando|
|70001	|Graham Zusi|
|70007	|Graham Zusi|
|70012	|Julian Green|
___
![Imgur](https://i.imgur.com/CZiWlYb.png)
![Imgur](https://i.imgur.com/GiAfR2H.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

SELECT customer.cust_name AS "Customer", customer.grade AS "Grade"   
FROM orders, salesman, customer   
WHERE orders.customer_id = customer.customer_id  
AND orders.salesman_id = salesman.salesman_id   
AND salesman.city IS NOT NULL   
AND customer.grade IS NOT NULL;

|Customer	    |Grade|
|---|---|
|Nick Rimando	|100|
|Geoff Cameron	|100|
|Brad Davis	    |200|
|Nick Rimando	|100|
|Fabian Johnson	|300|
|Geoff Cameron	|100|
|Jozy Altidor	|200|
|Nick Rimando	|100|
|Graham Zusi	    |200|
|Graham Zusi	    |200|
|Julian Green	|300|
___
![Imgur](https://i.imgur.com/GViFwcv.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

SELECT customer.cust_name AS "Customer", customer.city AS "City",   
salesman.name AS "Salesman", salesman.commission   
FROM customer,salesman  
WHERE customer.salesman_id = salesman.salesman_id   
AND salesman.commission   
BETWEEN .12 AND .14;

|Customer	    |City		|Salesman	|commission|
|---|---|---|---|
|Graham Zusi	    |California	|Nail Knite	|0.13|
|Julian Green	|London		|Nail Knite	|0.13|
|Fabian Johnson	|Paris		|Mc Lyon		|0.14|
|Geoff Cameron	|Berlin		|Lauson Hen	|0.12|
|Jozy Altidor	|Moscow		|Paul Adam	|0.13|
___
![Imgur](https://i.imgur.com/InpyWxX.png)
![Imgur](https://i.imgur.com/VXiYu3r.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

SELECT ord_no, cust_name, commission AS "Commission%",   purch_amt*commission AS "Commission"   
FROM salesman,orders,customer  
WHERE orders.customer_id = customer.customer_id   
AND orders.salesman_id = salesman.salesman_id   
AND customer.grade>=200;

|ord_no	|cust_name	    |Commission%	|Commission|
|---|---|---|---|
|70005	|Brad Davis	    |0.15		|360.0900|
|70010	|Fabian Johnson	|0.14		|277.6802|
|70011	|Jozy Altidor	|0.13		|9.7877|
|70001	|Graham Zusi	    |0.13		|19.5650|
|70007	|Graham Zusi	    |0.13		|123.3050|
|70012	|Julian Green	|0.13		|32.5585|
___
![Imgur](https://i.imgur.com/g03K5vq.png)
![Imgur](https://i.imgur.com/75Q38ei.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

SELECT *  
FROM customer a,orders  b   
WHERE a.customer_id=b.customer_id  
AND b.ord_date='2012-10-05';  

|customer_id	|cust_name	    |city		|grade	    |salesman_id	|ord_no	    |purch_amt	|ord_date	|customer_id	|salesman_id|
|---|---|---|---|---|---|---|---|---|---|
|3002		|Nick Rimando	|New York	|100	        |5001	    |70002	    |65.26		|2012-10-05	|3002		|5001|
|3005		|Graham Zusi	    |California	|200	        |5002	    |70001	    |150.50		|2012-10-05	|3005		|5002|
___