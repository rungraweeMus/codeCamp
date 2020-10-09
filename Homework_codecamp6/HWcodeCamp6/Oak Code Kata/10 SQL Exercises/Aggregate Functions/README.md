# SQL Exercises
## Aggregate Functions
![Imgur](https://i.imgur.com/iqJYb0j.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   
SELECT SUM (purch_amt)   
FROM orders;

| sum |
| --- |
| 17541.18 |

___
![Imgur](https://i.imgur.com/Rh7FluA.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   
SELECT AVG (purch_amt)   
FROM orders;

| avg |
| --- |
| 1461.7650000000000000 |
___
![Imgur](https://i.imgur.com/dfe3hES.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   
SELECT COUNT (DISTINCT salesman_id)   
FROM orders;

| count |
| --- |
| 6 |
___
![Imgur](https://i.imgur.com/mCTf6ou.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   
SELECT COUNT(*)   
FROM customer;  

| count |
| --- |
| 8 |
___
![Imgur](https://i.imgur.com/NpbDSlM.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   
SELECT COUNT (ALL grade)   
FROM customer;  

| count |
| --- |
| 7 |
___
![Imgur](https://i.imgur.com/sNpb2vU.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   
SELECT MAX (purch_amt)   
FROM orders;  

| max |
| --- |
| 5760.00 |
___
![Imgur](https://i.imgur.com/z3TtqRY.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   
SELECT MIN(purch_amt)   
FROM orders;

| min |
| --- |
| 65.26 |
___
![Imgur](https://i.imgur.com/zPycVdY.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   
SELECT city,MAX(grade)   
FROM customer   
GROUP BY city;

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

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   
SELECT customer_id, MAX(purch_amt)   
FROM orders   
GROUP BY customer_id;

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

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   
SELECT customer_id, ord_date, MAX(purch_amt)   
FROM orders   
GROUP BY customer_id, ord_date;  

|customer_id	|ord_date	|max|
|---|---|---|
|3002		|2012-10-05	|65.26|
|3003		|2012-08-17	|75.29|
|3005		|2012-10-05	|150.50|
|3007		|2012-07-27	|2400.60|
|3009		|2012-08-17	|110.50|
|3001		|2012-09-10	|270.65|
|3002		|2012-09-10	|5760.00|
|3005		|2012-09-10	|948.50|
|3009		|2012-10-10	|2480.40|
|3008		|2012-06-27	|250.45|
|3004		|2012-10-10	|1983.43|
|3002		|2012-04-25	|3045.60|

___
![Imgur](https://i.imgur.com/dDw63E7.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**     
SELECT salesman_id, MAX(purch_amt)   
FROM orders  
WHERE ord_date = '2012-08-17'   
GROUP BY salesman_id;

|salesman_id|	max|
|---|---|
|5003	|110.50|
|5007	|75.29|
___
![Imgur](https://i.imgur.com/nd0AXvw.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**     
SELECT customer_id, ord_date, MAX(purch_amt)   
FROM orders   
GROUP BY customer_id, ord_date   
HAVING MAX(purch_amt) > 2000.00;

|customer_id|	ord_date	|max|
|---|---|---|
|3007|	2012-07-27|	2400.60|
|3009|	2012-10-10|	2480.40|
|3002|	2012-09-10|	5760.00|
|3002|	2012-04-25|	3045.60|
___
![Imgur](https://i.imgur.com/f2YNsaZ.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**     
SELECT customer_id, ord_date, MAX(purch_amt)   
FROM orders   
GROUP BY customer_id, ord_date   
HAVING MAX(purch_amt)   
BETWEEN 2000 AND 6000;

|customer_id|	ord_date	|max|
|---|---|---|
|3007|	2012-07-27|	2400.60|
|3009|	2012-10-10|	2480.40|
|3002|	2012-09-10|	5760.00|
|3002|	2012-04-25|	3045.60|

___
![Imgur](https://i.imgur.com/ZeDpbaZ.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**     
SELECT customer_id, ord_date, MAX(purch_amt)   
FROM orders   
GROUP BY customer_id, ord_date   
HAVING MAX(purch_amt)   
IN (2000 ,3000,5760, 6000);

customer_id|	ord_date	|max|
|---|---|---|
|3002|	2012-09-10|	5760.00|

___
![Imgur](https://i.imgur.com/LjnUruY.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**     
SELECT customer_id, MAX(purch_amt)   
FROM orders   
WHERE customer_id   
BETWEEN 3002 and 3007   
GROUP BY customer_id;  

|customer_id|	max|
|---|---|
|3003|	75.29|
|3002|	5760.0|0
|3005|	948.50|
|3004|	1983.43|
|3007|	2400.60|
___
![Imgur](https://i.imgur.com/0ASSYwM.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**     
SELECT customer_id, MAX(purch_amt)   
FROM orders   
WHERE customer_id   
BETWEEN 3002 and 3007   
GROUP BY customer_id   
HAVING MAX(purch_amt)>1000;  

|customer_id|	max|
|---|---|
|3002|	5760.00|
|3004|	1983.43|
|3007|	2400.60|
___
![Imgur](https://i.imgur.com/1gRGq4P.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**     
SELECT salesman_id, MAX(purch_amt)   
FROM orders   
GROUP BY salesman_id   
HAVING salesman_id   
BETWEEN 5003 AND 5008;

|salesman_id|	max|
|---|---|
|5006|	1983.43|
|5003|	2480.40|
|5005|	270.65|
|5007|	75.29|
___
![Imgur](https://i.imgur.com/AnmJZ0U.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**     
SELECT COUNT(*)   
FROM orders   
WHERE ord_date = '2012-08-17';  

|count|
|---|
|2|
___
![Imgur](https://i.imgur.com/a234zev.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**     
SELECT COUNT(*)   
FROM salesman   
WHERE city IS NOT NULL;  

|count|
|---|
|6|
___
![Imgur](https://i.imgur.com/yJE759Y.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**     
SELECT ord_date, salesman_id, COUNT(*)   
FROM orders   
GROUP BY ord_date, salesman_id;  

|ord_date	|salesman_id	|count|
|---|---|---|
|2012-07-27	|5001		|1|
|2012-08-17	|5007		|1|
|2012-04-25	|5001		|1|
|2012-09-10	|5002		|1|
|2012-10-05	|5002		|1|
|2012-10-10	|5003		|1|
|2012-09-10	|5005		|1|
|2012-08-17	|5003		|1|
|2012-06-27	|5002		|1|
|2012-09-10	|5001		|1|
|2012-10-05	|5001		|1|
|2012-10-10	|5006		|1|
___
![Imgur](https://i.imgur.com/7e5aJxd.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**         
SELECT AVG(pro_price) AS "Average Price"   
FROM item_mast;

|Average Price|
|---|
|1435.0000000000000000|
___
![Imgur](https://i.imgur.com/S8AxTxs.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**       
SELECT COUNT(*) AS "Number of Products"   
FROM item_mast   
WHERE pro_price >= 350;  

|Number of Products|
|---|
|8|
___
![Imgur](https://i.imgur.com/fKAOOGd.png)  

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**     
SELECT AVG(pro_price) AS "Average Price", pro_com AS "Company ID"   
FROM item_mast   
GROUP BY pro_com;
 
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

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**         
SELECT SUM(dpt_allotment)   
FROM emp_department;  

|sum|
|---|
|450000|
___
![Imgur](https://i.imgur.com/P3wL5Fj.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   
SELECT emp_dept, COUNT(*)   
FROM emp_details   
GROUP BY emp_dept;  

|emp_dept|	count|
|---|---|
|47|	3|
|27|	2|
|63	|3|
|57|	5|
___