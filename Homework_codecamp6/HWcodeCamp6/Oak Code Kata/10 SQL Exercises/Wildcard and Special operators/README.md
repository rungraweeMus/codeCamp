# SQL Exercises
## Wildcard and Special operators
![Imgur](https://i.imgur.com/PsFgi5E.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  

    SELECT *   
    FROM salesman  
    WHERE city = 'Paris'  
    OR city = 'Rome';  

|salesman_id|name		|city	|commission|
|---|---|---|---|
|5002		|Nail Knite	|Paris	|0.13|
|5006		|Mc Lyon		|Paris	|0.14|
|5007		|Paul Adam	|Rome	|0.13|
___
![Imgur](https://i.imgur.com/DmIrI6v.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   

    SELECT *   
    FROM salesman   
    WHERE city IN ('Paris','Rome');  

|salesman_id	|name		|city	|commission|
|---|---|---|---|
|5002		|Nail Knite	|Paris	|0.13|
|5006		|Mc Lyon		|Paris	|0.14|
|5007		|Paul Adam	|Rome	|0.13|
___
![Imgur](https://i.imgur.com/vEqNm0x.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   

    SELECT *  
    FROM salesman   
    WHERE NOT city  
    IN ('Paris','Rome');  

|salesman_id|name	|city		|commission|
|---|---|---|---|
|5001		|James Hoog|New York	|0.15|
|5005		|Pit Alex|London		|0.11|
|5003		|Lauson Hen|San Jose	|0.12|
___
![Imgur](https://i.imgur.com/5zIoK4A.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  

    SELECT *   
    FROM customer   
    WHERE customer_id   
    IN (3007,3008,3009);

|customer_id	|cust_name	|city		|grade	   |salesman_id|
|---|---|---|---|---|
|3007		|Brad Davis	|New York	|200		   |5001|
|3008		|Julian Green|  London	|	300		|5002|
|3009		|Geoff Cameron|	Berlin	|	100		|5003|

___
![Imgur](https://i.imgur.com/0hFNJnw.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   

    SELECT *  
    FROM salesman  
    WHERE commission   
    BETWEEN 0.12 AND 0.14;  

|salesman_id |    name    |   city   | commission |
|---|---|---|---|
|5002 | Nail Knite | Paris    |       0.13|
|5006 | Mc Lyon    | Paris    |       0.14|
|5007 | Paul Adam  | Rome     |       0.13|
|5003 | Lauson Hen | San Jose |       0.12|
___
![Imgur](https://i.imgur.com/q7bkdve.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   

    SELECT *   
    FROM orders   
    WHERE (purch_amt BETWEEN 500 AND 4000)  
    AND NOT purch_amt IN (948.50,1983.43);  

|ord_no	|purch_amt	|ord_date	|customer_id|salesman_id|
|---|---|---|---|---|
|70005	|2400.60		|2012-07-27	|3007		|5001|
|70003	|2480.40		|2012-10-10	|3009		|5003|
|70013	|3045.60		|2012-04-25	|3002		|5001|

___
![Imgur](https://i.imgur.com/yV4jLAC.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer** 

    SELECT *   
    FROM salesman   
    WHERE name BETWEEN 'A' and 'K';  

|salesman_id	|name	    |city	    |commission|
|---|---|---|---|
|5001	    |James Hoog	|New York	|0.15|
___
![Imgur](https://i.imgur.com/piZtsAH.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**    

    SELECT *   
    FROM salesman   
    WHERE name NOT  
    BETWEEN 'A' and 'L';  

| salesman_id |    name    |   city   | commission |
|---|---|---|---|
|        5002 | Nail Knite | Paris    |       0.13|
|        5005 | Pit Alex   | London   |       0.11|
|        5006 | Mc Lyon    | Paris    |       0.14|
|        5007 | Paul Adam  | Rome     |       0.13|
|        5003 | Lauson Hen | San Jose |       0.12|
___
![Imgur](https://i.imgur.com/cr6jQNb.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

    SELECT *  
    FROM customer   
    WHERE cust_name LIKE 'B%';  

|customer_id	|cust_name	|city		|grade	|salesman_id|
|---|---|---|---|---|
|3007		|Brad Davis	|New York	|200	    |5001|
|3001		|Brad Guzan	|London		|	    |5005|
___
![Imgur](https://i.imgur.com/yAeiZch.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   

    SELECT *   
    FROM customer   
    WHERE cust_name LIKE '%n';      

|customer_id|cust_name		  |  city	|grade	|salesman_id|
|---|---|---|---|---|
|3008		|Julian Green	|	London	|300	    |5002|
|3004		|Fabian Johnson	|	Paris	|300	    |5006|
|3009		|Geoff Cameron	|	Berlin	|100	    |5003|
|3001		|Brad Guzan		  |  London	|	    |5005|
___
![Imgur](https://i.imgur.com/R5O5rFp.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

    SELECT *   
    FROM salesman   
    WHERE name LIKE 'N__l%';  

|salesman_id	|name		|city	|commission|
|---|---|---|---|
|5002		|Nail Knite	|Paris	|0.13|
___
![Imgur](https://i.imgur.com/hmf4lkt.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   

    SELECT *   
    FROM testtable   
    WHERE col1 LIKE '%/_%'   
    ESCAPE '/';  

|col1|
|---|
|A001/DJ-402\44_/100/2015|
|A001_\DJ-402\44_/100/2015|
|A001_DJ-402-2014-2015|
|A002_DJ-401-2014-2015|
|A001/DJ_401|
|A001/DJ_402\44|
|A001/DJ_402\44\2015|
|A001/DJ_402\45\2015%100|
|A001/DJ_402%45\2015/300|
|A001/DJ-402\44_/100/2015|
|A001_\DJ-402\44_/100/2015|
|A001_DJ-402-2014-2015|
|A002_DJ-401-2014-2015|
|A001/DJ_401|
|A001/DJ_402\44|
|A001/DJ_402\44\2015|
|A001/DJ_402\45\2015%100|
|A001/DJ_402%45\2015/300|
___
![Imgur](https://i.imgur.com/nH5UyZF.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   

    SELECT *  
    FROM testtable   
    WHERE col1   
    NOT LIKE '%/_%'  
    ESCAPE '/';  

|col1|
|---|
|A001/DJ-402%45\2015/200|
|A001/DJ-402\44|
|A001/DJ-402%45\2015/200|
|A001/DJ-402\44|
___
![Imgur](https://i.imgur.com/eDo5Cbf.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  

    SELECT *   
    FROM testtable  
    WHERE col1   
    LIKE '%//%'   
    ESCAPE '/';  

|col1|
|---|
|A001/DJ-402\44_/100/2015|
|A001_\DJ-402\44_/100/2015|
|A001/DJ_401|
|A001/DJ_402\44|
|A001/DJ_402\44\2015|
|A001/DJ-402%45\2015/200|
|A001/DJ_402\45\2015%100|
|A001/DJ_402%45\2015/300|
|A001/DJ-402\44|
___
![Imgur](https://i.imgur.com/vmb0GpI.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   

    SELECT *   
    FROM testtable  
    WHERE col1   
    NOT LIKE '%//%'   
    ESCAPE '/';  

|col1|
|---|
|A001_DJ-402-2014-2015|
|A002_DJ-401-2014-2015|
___
![Imgur](https://i.imgur.com/oHHfDQi.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

    SELECT *   
    FROM testtable   
    WHERE col1   
    LIKE '%/_//%'   
    ESCAPE '/';  

|col1|
|---|
|A001/DJ-402\44_/100/2015|
|A001_\DJ-402\44_/100/2015|
___
![Imgur](https://i.imgur.com/ry1C4E0.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   

    SELECT *  
    FROM testtable   
    WHERE col1   
    NOT LIKE '%/_//%'   
    ESCAPE '/';  

|col1|
|---|
|A001_DJ-402-2014-2015|
|A002_DJ-401-2014-2015|
|A001/DJ_401|
|A001/DJ_402\44|
|A001/DJ_402\44\2015|
|A001/DJ-402%45\2015/2|
|A001/DJ_402\45\2015%1|
|A001/DJ_402%45\2015/3|
|A001/DJ-402\44|
___
![Imgur](https://i.imgur.com/6EPGpY2.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer** 

    SELECT *   
    FROM testtable   
    WHERE col1   
    LIKE '%/%%' ESCAPE'/';  

|col1|
|---|
|A001/DJ-402%45\2015/200||
|A001/DJ_402\45\2015%100||
|A001/DJ_402%45\2015/300|
___
![Imgur](https://i.imgur.com/PnUxpBq.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   

    SELECT *   
    FROM testtable   
    WHERE col1   
    NOT LIKE '%/%%'  
    ESCAPE'/';  

|col1|
|---|
|A001/DJ-402\44_/100/2015|
|A001_\DJ-402\44_/100/2015|
|A001_DJ-402-2014-2015|
|A002_DJ-401-2014-2015|
|A001/DJ_401|
|A001/DJ_402\44|
|A001/DJ_402\44\2015|
|A001/DJ-402\44|
___
![Imgur](https://i.imgur.com/zhlkTeI.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  

    SELECT *   
    FROM customer   
    WHERE grade IS NULL;  

|customer_id|cust_name	|city	|grade|	salesman_id|
|---|---|---|---|---|
|3001		|Brad Guzan	|London	|	 |  5005|
___
![Imgur](https://i.imgur.com/6xYvbnk.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   

    SELECT *   
    FROM customer   
    WHERE NOT grade IS NULL;  

| customer_id |   cust_name    |    city    | grade | salesman_id|
|------|--------|-----|----|----|
|        3002 | Nick Rimando   | New York   |   100 |        5001|
|        3007 | Brad Davis     | New York   |   200 |        5001|
|        3005 | Graham Zusi    | California |   200 |        5002|
|        3008 | Julian Green   | London     |   300 |        5002|
|        3004 | Fabian Johnson | Paris      |   300 |        5006|
|        3009 | Geoff Cameron  | Berlin     |   100 |        5003|
|        3003 | Jozy Altidor   | Moscow     |   200 |        5007|
        
___
![Imgur](https://i.imgur.com/HBLxDC5.png)

![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   

    SELECT *   
    FROM emp_details   
    WHERE emp_lname   
    LIKE 'D%';  

|emp_idno|	emp_fname|emp_lname	|emp_dept|
|---|---|---|---|
|843795	|	Enric	|Dosio		|57|
|444527	|	Joseph	|Dosni		|47|
___