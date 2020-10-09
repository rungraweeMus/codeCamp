# SQL Exercises
## Formatting Query Output
![Imgur](https://i.imgur.com/VG41y8X.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   

SELECT salesman_id, name, city, '%', commission*100   FROM salesman;

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

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  

SELECT ' For',ord_date,',there are',   
COUNT (DISTINCT ord_no),'orders.'   
FROM orders   
GROUP BY ord_date;  

|?column?	|ord_date	|?column?	|count	|?column?|
|---|---|---|---|---|----|
|For		    |2012-04-25	|,there are	|1	    |orders.|
|For		    |2012-06-27	|,there are	|1	    |orders.|
|For		    |2012-07-27	|,there are	|1	    |orders.|
|For		    |2012-08-17	|,there are	|2	    |orders.|
|For		    |2012-09-10	|,there are	|3	    |orders.|
|For		    |2012-10-05	|,there are	|2	    |orders.|
|For		    |2012-10-10	|,there are	|2	    |orders.|
___
![Imgur](https://i.imgur.com/1yqDbY6.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   

SELECT *   
FROM orders   
ORDER BY ord_no;  

|ord_no	|purch_amt	|ord_date	|customer_id	|salesman_id|
|---|---|---|---|---|
|70001	|150.50	    |2012-10-05	|3005	    |5002|
|70002	|65.26	    |2012-10-05	|3002	    |5001|
|70003	|2480.40	    |2012-10-10	|3009	    |5003|
|70004	|110.50	    |2012-08-17	|3009	    |5003|
|70005	|2400.60	    |2012-07-27	|3007	    |5001|
|70007	|948.50	    |2012-09-10	|3005	    |5002|
|70008	|5760.00	    |2012-09-10	|3002	    |5001|
|70009	|270.65	    |2012-09-10	|3001	    |5005|
|70010	|1983.43	    |2012-10-10	|3004	    |5006|
|70011	|75.29	    |2012-08-17	|3003	    |5007|
|70012	|250.45	    |2012-06-27	|3008	    |5002|
|70013	|3045.60	    |2012-04-25	|3002	    |5001|
___
![Imgur](https://i.imgur.com/Jdpaym2.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  

SELECT *   
FROM orders   
ORDER BY ord_date DESC;  

|ord_no	|purch_amt	|ord_date	|customer_id	|salesman_id|
|---|---|---|---|---|
|70010	|1983.43	    |2012-10-10	|3004	    |5006|
|70003	|2480.40	    |2012-10-10	|3009	    |5003|
|70002	|65.26	    |2012-10-05	|3002	    |5001|
|70001	|150.50	    |2012-10-05	|3005	    |5002|
|70009	|270.65	    |2012-09-10	|3001	    |5005|
|70008	|5760.00	    |2012-09-10	|3002	    |5001|
|70007	|948.50	    |2012-09-10	|3005	    |5002|
|70011	|75.29	    |2012-08-17	|3003	    |5007|
|70004	|110.50	    |2012-08-17	|3009	    |5003|
|70005	|2400.60	    |2012-07-27	|3007	    |5001|
|70012	|250.45	    |2012-06-27	|3008	    |5002|
|70013	|3045.60	    |2012-04-25	|3002	    |5001|

___
![Imgur](https://i.imgur.com/zDGw4B2.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  

SELECT *   
FROM orders   
ORDER BY ord_date, purch_amt DESC;  

|ord_no	|purch_amt	|ord_date	|customer_id	|salesman_id|
|---|---|---|---|---|
|70013	|3045.60	    |2012-04-25	|3002	    |5001|
|70012	|250.45	    |2012-06-27	|3008	    |5002|
|70005	|2400.60	    |2012-07-27	|3007	    |5001|
|70004	|110.50	    |2012-08-17	|3009	    |5003|
|70011	|75.29	    |2012-08-17	|3003	    |5007|
|70008	|5760.00	    |2012-09-10	|3002	    |5001|
|70007	|948.50	    |2012-09-10	|3005	    |5002|
|70009	|270.65	    |2012-09-10	|3001	    |5005|
|70001	|150.50	    |2012-10-05	|3005	    |5002|
|70002	|65.26	    |2012-10-05	|3002	    |5001|
|70003	|2480.40	    |2012-10-10	|3009	    |5003|
|70010	|1983.43	    |2012-10-10	|3004	    |5006|
___
![Imgur](https://i.imgur.com/fuOMiHn.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer** 

SELECT cust_name, city, grade   
FROM customer   
ORDER BY customer_id;  

|cust_name	    |city	    |grade|
|---|---|---|
|Brad Guzan	    |London	    ||
|Nick Rimando	|New York	|100|
|Jozy Altidor	|Moscow	    |200|
|Fabian Johnson	|Paris	    |300|
|Graham Zusi	    |California	|200|
|Brad Davis	    |New York	    |200|
|Julian Green	|London	    |300|
|Geoff Cameron	|Berlin	    |100|
___
![Imgur](https://i.imgur.com/HU2yn8K.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer** 

SELECT salesman_id, ord_date, MAX(purch_amt)   
FROM orders   
GROUP BY salesman_id, ord_date   
ORDER BY salesman_id,ord_date;  

|salesman_id	|ord_date	|max|
|---|---|---|
|5001		|2012-04-25	|3045.60|
|5001		|2012-07-27	|2400.60|
|5001		|2012-09-10	|5760.00|
|5001		|2012-10-05	|65.26|
|5002		|2012-06-27	|250.45|
|5002		|2012-09-10	|948.50|
|5002		|2012-10-05	|150.50|
|5003		|2012-08-17	|110.50|
|5003		|2012-10-10	|2480.40|
|5005		|2012-09-10	|270.65|
|5006		|2012-10-10	|1983.43|
|5007		|2012-08-17	|75.29|
___
![Imgur](https://i.imgur.com/lfL5qzX.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer** 

SELECT cust_name, city, grade   
FROM customer   
ORDER BY 3 DESC;  

|cust_name	    |city		|grade|
|---|---|---|
|Brad Guzan	    |London	    ||
|Fabian Johnson	|Paris		|300|
|Julian Green	|London		|300|
|Brad Davis	    |New York	|200|
|Jozy Altidor	|Moscow		|200|
|Graham Zusi	    |California	|200|
|Nick Rimando	|New York	|100|
|Geoff Cameron	|Berlin		|100|
___
![Imgur](https://i.imgur.com/A58pvlR.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   

SELECT customer_id, COUNT(DISTINCT ord_no), MAX(purch_amt)   
FROM orders   
GROUP BY customer_id   
ORDER BY 2 DESC;  

|customer_id|count	|max|
|---|---|---|
|3002	   |3	    |5760.00|
|3009	   |2	    |2480.40|
|3005	   |2	    |948.50|
|3004	   |1	    |1983.43|
|3001	   |1	    |270.65|
|3007	   |1	    |2400.60|
|3008	   |1	    |250.45|
|3003	   |1	    |75.29|
___
![Imgur](https://i.imgur.com/D2NRZBp.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   

SELECT ord_date, SUM(purch_amt), SUM(purch_amt)*.15   
FROM orders   
GROUP BY ord_date   
ORDER BY ord_date;  

|ord_date	|sum     |?column?|
|---|---|---|
|2012-04-25	|3045.60	|456.8400|
|2012-06-27	|250.45	|37.5675|
|2012-07-27	|2400.60	|360.0900|
|2012-08-17	|185.79	|27.8685|
|2012-09-10	|6979.15	|1046.8725|
|2012-10-05	|215.76	|32.3640|
|2012-10-10	|4463.83	|669.5745|
___