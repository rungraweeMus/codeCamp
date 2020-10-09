# SQL Exercises
## Retrieve data from tables
1. Write a SQL statement to display all the information of all salesmen.   

    Sample table: salesman
    ![Imgur](https://i.imgur.com/5OWQ9MY.png)
 ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  
 SELECT * FROM salesman;

 ___
2. Write a SQL statement to display a string "This is SQL Exercise, Practice and Solution".

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   
  SELECT "This is SQL Exercise, Practice and Solution";  

    |?column?|  
    |-----------|  
    |This is SQL Exercise, Practice and Solution|
___
3. Write a query to display three numbers in three columns.  
   
   ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   
   SELECT 8, 14, 15;
    |?column?|  
    |-----------|  
    |15|
___
4. Write a query to display the sum of two numbers 10 and 15 from RDMS sever. 

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   
    SELECT 10 + 15;
    |?column?|  
    |-----------|  
    |25|
___
5. Write a query to display the result of an arithmetic expression.  
   
    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   
    SELECT 12 + 15 * 2 - 7;

    |?column?|  
    |-----------|  
    |35|
___
6. Write a SQL statement to display specific columns like name and commission for all the salesmen. 

    Sample table: salesman
        ![Imgur](https://i.imgur.com/5OWQ9MY.png)
    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  
    SELECT name, commission
FROM salesman; 

    |name|	commission|
    |---|---|
    |James Hoog|	0.15|
    |Nail Knite|	0.13|
    |Pit Alex|	0.11|
    |Mc Lyon|	0.14|
    |Paul Adam|	0.13|
    |Lauson Hen|	0.12|
___
7. Write a query to display the columns in a specific order like order date, salesman id, order number and purchase amount from for all the orders. 
   
   Sample table : orders
![Imgur](https://i.imgur.com/mzhsP3B.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  
        SELECT ord_date, salesman_id, ord_no, purch_amt  
FROM orders;   

    |ord_date|	salesman_id|	ord_no|	purch_amt|
    |---|---|---|---|
    |2012-09-10	|5005	|70009	|270.65|
    |2012-10-05	|5001	|70002	|65.26|
    |2012-08-17	|5003	|70004	|110.50|
    |2012-07-27	|5001	|70005	|2400.6|
    |2012-09-10	|5001	|70008	|5760.0|
    |2012-10-10	|5006	|70010	|1983.4|
    |2012-10-10	|5003	|70003	|2480.4|
    |2012-08-17	|5007	|70011	|75.29|
    |2012-04-25	|5001	|70013	|3045.6|
    |2012-10-05	|5002	|70001	|150.50|
    |2012-09-10	|5002	|70007	|948.50|
    |2012-06-27	|5002	|70012	|250.45|
___
8. Write a query which will retrieve the value of salesman id of all salesmen, getting orders from the customers in orders table without any repeats.    
   
    Sample table : orders
![Imgur](https://i.imgur.com/mzhsP3B.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  
        SELECT DISTINCT salesman_id  
FROM orders; 

    |salesman_id|
    |---|
   |5006|
   |5002|
   |5003|
   |5001|
   |5005|
   |5007|
___
9. Write a SQL statement to display names and city of salesman, who belongs to the city of Paris.  
    
    Sample table: salesman
    ![Imgur](https://i.imgur.com/5OWQ9MY.png)
 ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  
 SELECT name,city FROM salesman   
 WHERE city='Paris';

    |name	|city|
    |---|---|
    |Nail Knite	|Paris|
    |Mc Lyon|Paris|
___
10. Write a SQL statement to display all the information for those customers with a grade of 200.   
    
    Sample table: customer
    ![Imgur](https://i.imgur.com/mOglYfz.png)
    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)
    **Answer**  
    SELECT *FROM customer  
    WHERE grade=200;

    |customer_id	|cust_name	   | city	    |grade	|salesman_id|
    |----|---|---|---|---|
    |3007	        |Brad Davis	  | New York	|200	  |  5001|
    |3005	        |Graham Zusi   |California	|200	  |  5002|
    |3003	        |Jozy Altidor  |Moscow	    |200	  |  5007|
___
11. Write a SQL query to display the order number followed by order date and the purchase amount for each order which will be delivered by the salesman who is holding the ID 5001.  
    
     Sample table : orders
    ![Imgur](https://i.imgur.com/mzhsP3B.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  
    SELECT ord_no, ord_date, purch_amt   
    FROM orders   
    WHERE salesman_id=5001;

    |ord_no|	ord_date	|purch_amt|
    |---|---|---|
    |70002	|2012-10-05|	65.26|
    |70005	|2012-07-27|	2400.60|
    |70008	|2012-09-10|	5760.00|
    |70013	|2012-04-25|	3045.60|
___
12. Write a SQL query to display the Nobel prizes for 1970.     

    Sample table: nobel_win
    ![Imgur](https://i.imgur.com/GXEBvP3.png)

     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  
    SELECT year,subject,winner   
    FROM nobel_win   
    WHERE year=1970; 

    |year	|subject	    |winner|
    |---|---|---|
    |1970	|Physics	    |Hannes Alfven|
    |1970	|Physics	    |Louis Neel|
    |1970	|Chemistry	|Luis Federico Leloir|
    |1970	|Physiology	|Julius Axelrod|
    |1970	|Physiology	|Ulf von Euler|
    |1970	|Physiology	|Bernard Katz|
    |1970	|Literature	|Aleksandr Solzhenitsyn|
    |1970	|Economics	|Paul Samuelson|
    |1970	|Physics	    |Hannes Alfven|
    |1970	|Physics	    |Louis Neel|
    |1970	|Chemistry	|Luis Federico Leloir|
    |1970	|Physiology	|Julius Axelrod|
    |1970	|Physiology	|Ulf von Euler|
    |1970	|Physiology	|Bernard Katz|
    |1970	|Literature	|Aleksandr Solzhenitsyn|
    |1970	|Economics	|Paul Samuelson|
___
13. Write a SQL query to know the winner of the 1971 prize for Literature. 
    
     Sample table: nobel_win
    ![Imgur](https://i.imgur.com/GXEBvP3.png)

     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**    
     SELECT DISTINCT winner  
    FROM nobel_win  
    WHERE year = 1971  
    AND subject = 'Literature';

    |winner|
    |---|
    |Pablo Neruda|
___
14. Write a SQL query to display the year and subject that won 'Dennis Gabor' his prize. 

    Sample table: nobel_win
    ![Imgur](https://i.imgur.com/GXEBvP3.png)

     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**     
     SELECT DISTINCT year, subject  
  FROM nobel_win  
 WHERE winner = 'Dennis Gabor';

    |year|	subject|
    |---|--|
    |1971|	Physics|
___
15. Write a SQL query to give the name of the 'Physics' winners since the year 1950.  
    
     Sample table: nobel_win
    ![Imgur](https://i.imgur.com/GXEBvP3.png)

     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**    
     SELECT DISTINCT winner   
     FROM nobel_win   
     WHERE year>=1950   
     AND subject='Physics';

    |winner|
    |---|
    |Dennis Gabor|
    |Hannes Alfven|
    |Johannes Georg Bednorz|
    |Louis Neel|
___
16. Write a SQL query to Show all the details (year, subject, winner, country ) of the Chemistry prize winners between the year 1965 to 1975 inclusive.  
    
     Sample table: nobel_win
    ![Imgur](https://i.imgur.com/GXEBvP3.png)

     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**     
     SELECT DISTINCT year, subject, winner,   country   
     FROM nobel_win       
     WHERE subject = 'Chemistry'   
     AND year>=1965   
     AND year<=1975;  

    |year|	subject	  |  winner	                |country|
    |---|---|---|---|
    |1970|	Chemistry	|Luis Federico Leloir	|France|
    |1971|	Chemistry	|Gerhard Herzberg	    |Germany|
___
17. Write a SQL query to show all details of the Prime Ministerial winners after 1972 of Menachem Begin and Yitzhak Rabin.
    
     Sample table: nobel_win
    ![Imgur](https://i.imgur.com/GXEBvP3.png)

     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   

     SELECT DISTINCT *   
     FROM nobel_win   
     WHERE year >1972   
     AND winner   
     IN ('Menachem Begin','Yitzhak Rabin'); 

    |year	|subject	|winner	    |country	|category|
    |---|---|---|---|---|
    |1978	|Peace  	|Menachem Begin |Israel	|Prime Minister|
    |1994	|Peace	    |Yitzhak Rabin |Israel	|Prime Minister|
___
18. Write a SQL query to show all the details of the winners with first name Louis.
    
    Sample table: nobel_win
    ![Imgur](https://i.imgur.com/GXEBvP3.png)

     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   

     SELECT DISTINCT *   
    FROM nobel_win  
    WHERE winner   
    LIKE 'Louis%';

    |year|	subject|	winner	   | country|	category|
    |---|---|----|---|---|
    |1970|	Physics|	Louis Neel|	France	|Scientist|
___
19. Write a SQL query to show all the winners in Physics for 1970 together with the winner of Economics for 1971.
    
    Sample table: nobel_win
    ![Imgur](https://i.imgur.com/GXEBvP3.png)

     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  
     SELECT *     
     FROM nobel_win      
     WHERE (subject ='Physics' AND year=1970)     
     UNION (SELECT * FROM nobel_win  WHERE (subject ='Economics' AND year=1971)); 

    |year|	subject|    winner	        country|	category|
    |---|---|---|---|
    |1970|	Physics|    Hannes Alfven	Sweden	|Scientist|
    |1970|	Physics|    Louis Neel	    France	|Scientist|
    |1971|	Economics|	Simon Kuznets	Russia	|Economist|
___
20. Write a SQL query to show all the winners of nobel prize in the year 1970 except the subject Physiology and Economics. 

     Sample table: nobel_win
    ![Imgur](https://i.imgur.com/GXEBvP3.png)

     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  
    SELECT DISTINCT *  
    FROM nobel_win   
    WHERE year=1970  
    AND subject 
    NOT IN('Physiology','Economics');

    |year|	subject	  |  winner	               | country	|category|
    |---|---|---|---|---|
    |1970|	Chemistry	|Luis Federico Leloir	|France	    |Scientist|
    |1970|	Literature|	Aleksandr Solzhenitsyn|	Russia  	|Linguist|
    |1970|	Physics	  |  Hannes Alfven	       | Sweden	    |Scientist|
    |1970|	Physics	  |  Louis Neel	           | France 	|Scientist|
___
21. Write a SQL query to show the winners of a 'Physiology' prize in an early year before 1971 together with winners of a 'Peace' prize in a later year on and after the 1974.  
    
     Sample table: nobel_win
    ![Imgur](https://i.imgur.com/GXEBvP3.png)

     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  
     SELECT *   
     FROM nobel_win   
     WHERE (subject ='Physiology' AND year<1971)   
     UNION (SELECT * FROM nobel_win WHERE (subject ='Peace' AND year>=1974));

    |year	|subject	|winner	        |country|	        category|
    |---|---|---|---|---|---|---|
    |1970	|Physiology	|Bernard Katz	|Germany|	        Scientist|
    |1970	|Physiology	|Julius Axelrod	|USA	|            Scientist|
    |1970	|Physiology	|Ulf von Euler	|Sweden |     	    Scientist|
    |1978	|Peace	    |Anwar al-Sadat	|Egypt	|            President|
    |1978	|Peace	    |Menachem Begin	|Israel	|            Prime Minister|
    |1994	|Peace	    |Yitzhak Rabin	|Israel |       	Prime Minister|
___
22. Write a SQL query to find all details of the prize won by Johannes Georg Bednorz. 

    Sample table: nobel_win
    ![Imgur](https://i.imgur.com/GXEBvP3.png)

     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  
     SELECT DISTINCT *   
     FROM nobel_win   
     WHERE winner='Johannes Georg Bednorz';

    |year	|subject	|winner	                |country	|category|
    |---|---|---|---|---|
    |1987	|Physics	|Johannes Georg Bednorz	|Germany	|Scientist|
___
23. Write a SQL query to find all the details of the nobel winners for the subject not started with the letter 'P' and arranged the list as the most recent comes first, then by name in order.   
    
    Sample table: nobel_win
    ![Imgur](https://i.imgur.com/GXEBvP3.png)

     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  
     SELECT DISTINCT *   
     FROM nobel_win   
     WHERE subject   
     NOT LIKE 'P%'   
     ORDER BY year DESC, winner;

    |year	|subject	    |winner	                |country	|category|
    |---|---|---|---|---|
    |1994	|Literature	    |Kenzaburo Oe	        |Japan	   |Linguist|
    |1994	|Economics	    |Reinhard Selten	    |Germany   |Economist|
    |1987	|Chemistry	    |Donald J. Cram	        |USA       |Scientist|
    |1987	|Chemistry	    |Jean-Marie Lehn	    |France	   |Scientist|
    |1987	|Literature	    |Joseph Brodsky	        |Russia	   |Linguist|
    |1987	|Economics	    |Robert Solow	        |USA       |Economist|
    |1971	|Chemistry	    |Gerhard Herzberg	    |Germany   |Scientist|
    |1971	|Literature	    |Pablo Neruda	        |Chile	   |Linguist|
    |1971	|Economics	    |Simon Kuznets	        |Russia	   |Economist|
    |1970	|Literature	    |Aleksandr Solzhenitsyn	|Russia	   |Linguist|
    |1970	|Chemistry	    |Luis Federico Leloir	|France	   |Scientist|
    |1970	|Economics	    |Paul Samuelson	        |USA	   |Economist|
___
24. Write a SQL query to find all the details of 1970 winners by the ordered to subject and winner name; but the list contain the subject Economics and Chemistry at last.
    
    Sample table: nobel_win
    ![Imgur](https://i.imgur.com/GXEBvP3.png)

     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  
     SELECT *   
     FROM nobel_win 
     WHERE year=1970   
     ORDER BY    
     CASE WHEN subject IN ('Economics','Chemistry')    
     THEN 1 ELSE 0 END ASC, subject, winner;

    |year	|subject		|winner				        |country	|category|
    |---|---|---|---|---|
    |1970	|Literature	    |Aleksandr Solzhenitsyn		|Russia		|Linguist|
    |1970	|Physics		|Hannes Alfven			    |Sweden		|Scientist|
    |1970	|Physics		|Louis Neel			        |France		|Scientist|
    |1970	|Physiology	    |Bernard Katz			    |Germany	|Scientist|
    |1970	|Physiology	    |Julius Axelrod			    |USA		|Scientist|
    |1970	|Physiology	    |Ulf von Euler			    |Sweden		|Scientist|
    |1970	|Chemistry	    |Luis Federico Leloir		|France		|Scientist|
    |1970	|Economics	    |Paul Samuelson			    |USA		|Economist|
___
25. Write a SQL query to find all the products with a price between Rs.200 and Rs.600. 
    
    Sample table: item_mast
    ![Imgur](https://i.imgur.com/l0cpNGc.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   
    SELECT *   
    FROM item_mast   
    WHERE pro_price   
    BETWEEN 200 AND 600;

    |pro_id	    |pro_name	        |pro_price	|pro_com|
    |---|---|---|---|
    |102	    |Key Board	        |450.00	   | 16|
    |103        |ZIP drive	        |250.00	   | 14|
    |104	    |Speaker	        |550.00	   | 16|
    |109	    |Refill cartridge	|350.00	   | 13|
    |110	    |Mouse	            |250.00	   | 12|
___
26. Write a SQL query to calculate the average price of all products of the manufacturer which code is 16. 
    
     Sample table: item_mast
    ![Imgur](https://i.imgur.com/l0cpNGc.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**     
    SELECT AVG(pro_price)   
    FROM item_mast  
    WHERE pro_com=16;

    |avg|
    |---|
    |500.0000000000000000|
___
27. Write a SQL query to find the item name and price in Rs.    
    
    Sample table: item_mast
    ![Imgur](https://i.imgur.com/l0cpNGc.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**     
    SELECT pro_name AS "Item Name", pro_price AS "Price in Rs."   
    FROM item_mast;

    |Item Name	        |Price in Rs.|
    |---|---|
    |Mother Board	    |3200.00|
    |Key Board	        |450.00|
    |ZIP drive	        |250.00|
    |Speaker	        |550.00|
    |Monitor	        |5000.00|
    |DVD drive	        |900.00|
    |CD drive	        |800.00|
    |Printer	        |2600.00|
    |Refill cartridge	|350.00|
    |Mouse	            |250.00|
___
28. Write a SQL query to display the name and price of all the items with a price is equal or more than Rs.250, and the list contain the larger price first and then by name in ascending order.    
    
    Sample table: item_mast
    ![Imgur](https://i.imgur.com/l0cpNGc.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**     
    SELECT pro_name, pro_price   
    FROM item_mast   
    WHERE pro_price >= 250   
    ORDER BY pro_price DESC, pro_name;

    |pro_name	   |pro_price|
    |---|---|
    |Monitor	       |5000.00|
    |Mother Board   |3200.00|
    |Printer	       |2600.00|
    |DVD drive	   |900.00|
    |CD drive	   |800.00|
    |Speaker	       |550.00|
    |Key Board	   |450.00|
    |Refill cartridg|350.00|
    |Mouse	       |250.00|
    |ZIP drive	   |250.00|
___
29. Write a SQL query to display the average price of the items for each company, showing only the company code. 
     
    Sample table: item_mast
    ![Imgur](https://i.imgur.com/l0cpNGc.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  

    SELECT AVG(pro_price), pro_com   
    FROM item_mast   
    GROUP BY pro_com;

    |avg	                    |pro_com|
    |---|---|
    |5000.0000000000000000	|11|
    |1475.0000000000000000	|13|
    |500.0000000000000000	|16|
    |3200.0000000000000000	|15|
    |650.0000000000000000	|12|
    |250.0000000000000000	|14|
___
30. Write a SQL query to find the name and price of the cheapest item(s).    
    
    Sample table: item_mast
    ![Imgur](https://i.imgur.com/l0cpNGc.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  

    SELECT pro_name, pro_price  
   FROM item_mast  
   WHERE pro_price = (SELECT MIN(pro_price) FROM item_mast);

    |pro_name	|pro_price|
    |--|---|
    | ZIP drive	|250.00|
    | Mouse	    |250.00|    
___
31. Write a query in SQL to find the last name of all employees, without duplicates.   
    
    Sample table: emp_details
    ![Imgur](https://i.imgur.com/nw1H6fP.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  
    SELECT DISTINCT emp_lname  
    FROM emp_details;

    |emp_lname|
    |---|
    |Sitaraman|
    |Dosni|
    |Emily|
    |Foster|
    |Saule|
    |Mardy|
    |Manuel|
    |Dosio|
    |Robbin|
    |Snappy|
    |Snares|
    |Gabrie|
___
32. Write a query in SQL to find the data of employees whose last name is 'Snares'.  
    
    Sample table: emp_details
    ![Imgur](https://i.imgur.com/nw1H6fP.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  
    SELECT *   
    FROM emp_details  
    WHERE emp_lname= 'Snares';

    |emp_idno	|emp_fname	|emp_lname	|emp_dept|
    |---|---|---|---|
    |526689	    |Carlos	    |Snares	    |63|
    |328717	    |Jhon	    |Snares	    |63|     
___
33. Write a query in SQL to display all the data of employees that work in the department 57. 
     
    Sample table: emp_details
    ![Imgur](https://i.imgur.com/nw1H6fP.png)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**  
    SELECT *   
    FROM emp_details   
    WHERE emp_dept= 57;

    |emp_idno	|emp_fname	|emp_lname	|emp_dept|
    |---|---|---|---|
    |839139	    |Maria	    |Foster	    |57|
    |127323	    |Michale	    |Robbin	    |57|
    |843795	    |Enric	    |Dosio	    |57|
    |847674	    |Kuleswar	|Sitaraman	|57|
    |555935	    |Alex	    |Manuel	    |57|
___