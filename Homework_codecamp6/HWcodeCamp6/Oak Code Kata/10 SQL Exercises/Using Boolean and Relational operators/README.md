# SQL Exercises
## Using Boolean and Relational operators
![Imgur](https://i.imgur.com/vFHJMM1.png)

 ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**    
 SELECT *   
 FROM customer   
 WHERE grade > 100;

|customer_id	|cust_name	  |  city	    |grade|	salesman_id|
|---|---|---|---|---|
|3007	    |Brad Davis	  |  New York	|200	 |   5001|
|3005	    |Graham Zusi	    |California	|200	 |   5002|
|3008	    |Julian Green	|London	    |300	 |   5002|
|3004	    |Fabian Johnson|	Paris	    |300	 |   5006|
|3003	    |Jozy Altidor	|Moscow	    |200	 |   5007|

___
![Imgur](https://i.imgur.com/pcTsEJZ.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  
SELECT *   
FROM customer   
WHERE city = 'New York'   
AND grade > 100;

|customer_id|	cust_name	|city		|grade		|salesman_id|
|---|---|---|---|---|
|3007		|Brad Davis	|New York	|200		    |5001|

___
![Imgur](https://i.imgur.com/2gRZJNY.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**    
SELECT *   
FROM customer  
WHERE city = 'New York'   
OR grade > 100;  

|customer_id	|cust_name	    |city		|grade	|salesman_id|
|---|---|---|---|---|
|3002		|Nick Rimando    |New York	|100		|5001|
|3007		|Brad Davis	    |New York	|200		|5001|
|3005		|Graham Zusi	    |California	|200		|5002|
|3008		|Julian Green    |London		|300		|5002|
|3004		|Fabian Johnson  |Paris		|300		|5006|
|3003		|Jozy Altidor    |Moscow		|200		|5007|
___
![Imgur](https://i.imgur.com/LJPzvSp.png)
![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  
SELECT *   
FROM customer   
WHERE city = 'New York'   
OR NOT grade>100;  

|customer_id	|cust_name	    |city	|	grade  | salesman_id|
|---|---|---|---|---|
|3002		|Nick Rimando	|New York|	100	   | 5001|
|3007		|Brad Davis	    |New York	|    200	   | 5001|
|3009		|Geoff Cameron	|Berlin	|	100	   | 5003|
___
![Imgur](https://i.imgur.com/Qa2GPQa.png)
![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  

SELECT *   
FROM customer   
WHERE NOT (city = 'New York' OR grade>100);  

|customer_id|cust_name	 |   city	|grade	|salesman_id|
|---|---|---|---|---|
|3009		|Geoff Cameron|	Berlin	|100	    |5003|
___
![Imgur](https://i.imgur.com/RMvw1e7.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  
SELECT *   
FROM  orders   
WHERE NOT ((ord_date ='2012-09-10'AND salesman_id > 5005)   
OR purch_amt > 1000.00);

ord_no|purch_amt|ord_date  |customer_id|salesman_id|
------|---------|----------|-----------|-----------|
 70009|   270.65|2012-09-10|       3001|       5005|
 70002|    65.26|2012-10-05|       3002|       5001|
 70004|   110.50|2012-08-17|       3009|       5003|
 70011|    75.29|2012-08-17|       3003|       5007|
 70001|   150.50|2012-10-05|       3005|       5002|
 70007|   948.50|2012-09-10|       3005|       5002|
 70012|   250.45|2012-06-27|       3008|       5002|

___
![Imgur](https://i.imgur.com/EyBXQSU.png)
![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  
SELECT salesman_id,name,city,commission   
FROM salesman  
WHERE (commission > 0.10 AND commission< 0.12);  

|salesman_id	|name	|city	|commission|
|---|---|---|---|
|5005		|Pit Alex|London	|0.11|

___
![Imgur](https://i.imgur.com/jsrtZZ1.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  
SELECT *   
FROM  orders   
WHERE(purch_amt<200   
OR NOT(ord_date>='2012-02-10'  
AND customer_id<3009));  

|ord_no	|purch_amt	|ord_date	|customer_id	|salesman_id|
|---|---|---|---|---|
|70002	|65.26		|2012-10-05	|3002		|5001|
|70004	|110.50		|2012-08-17	|3009		|5003|
|70003	|2480.40		|2012-10-10	|3009		|5003|
|70011	|75.29		|2012-08-17	|3003		|5007|
|70001	|150.50		|2012-10-05	|3005		|5002|

___
![Imgur](https://i.imgur.com/ZRgWCVl.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  
SELECT *   
FROM  orders  
WHERE NOT((ord_date ='2012-08-17'  
OR customer_id>3005)   
AND purch_amt<1000);

|ord_no	|purch_amt	|ord_date	|customer_id|	salesman_id|
|---|---|---|---|---|
|70009	|270.65		|2012-09-10	|3001|		5005|
|70002	|65.26		|2012-10-05	|3002|		5001|
|70005	|2400.60		|2012-07-27	|3007|		5001|
|70008	|5760.00		|2012-09-10	|3002|		5001|
|70010	|1983.43		|2012-10-10	|3004|		5006|
|70003	|2480.40		|2012-10-10	|3009|		5003|
|70013	|3045.60		|2012-04-25	|3002|		5001|
|70001	|150.50		|2012-10-05	|3005|		5002|
|70007	|948.50		|2012-09-10	|3005|		5002|

___
![Imgur](https://i.imgur.com/VCnoCaQ.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   
SELECT ord_no,purch_amt,   
(100*purch_amt)/6000 AS "Achieved %",    
 (100*(6000-purch_amt)/6000) AS "Unachieved %"   
 FROM  orders   
 WHERE (100*purch_amt)/6000>50;  

|ord_no	|purch_amt	|Achieved %			|Unachieved %|
|---|---|---|---|
|70008	|5760.00		|96.0000000000000000	|4.0000000000000000|
|70013	|3045.60		|50.7600000000000000	|49.2400000000000000|

___
![Imgur](https://i.imgur.com/v8d994f.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   
SELECT *    
FROM emp_details    
WHERE emp_lname ='Dosni'   
OR emp_lname= 'Mardy';  

|emp_idno	|emp_fname	|emp_lname	|emp_dept|
|---|---|---|---|
|444527		|Joseph		|Dosni		|47|
|539569		|George		|Mardy		|27|

___
![Imgur](https://i.imgur.com/jPTfCYq.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  
SELECT *    
FROM emp_details   
WHERE emp_dept = 47   
OR emp_dept = 63;  

|emp_idno	|emp_fname	|emp_lname	|emp_dept|
|---|---|---|---|
|526689		|Carlos		|Snares		|63|
|328717		|Jhon		|Snares		|63|
|444527		|Joseph		|Dosni		|47|
|659831		|Zanifer		|Emily		|47|
|748681		|Henrey		|Gabriel		|47|
|733843		|Mario		|Saule		|63|
___
