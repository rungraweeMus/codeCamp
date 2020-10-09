# SQL Exercises
## FILTERING and SORTING on HR Database
**Sample table: employees**

![Imgur](https://i.imgur.com/o0GLrdA.png)
![Imgur](https://i.imgur.com/qdap0tQ.png)
___
**Sample table: departments**

![Imgur](https://i.imgur.com/izowzaD.png)
___
**Sample table: job_history**

![Imgur](https://i.imgur.com/5vKakb3.png)

___
**Sample table: locations**

![Imgur](https://i.imgur.com/VNoA6uq.png)

___
**Sample table: jobs**

![Imgur](https://i.imgur.com/AELzcUQ.png)
___

1. Write a query in SQL to display the full name (first and last name), and salary for those employees who earn below 6000. 

    **database table:** employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   

        SELECT first_name ||' '||last_name AS Full_Name, salary  
            FROM employees  
            WHERE salary < 6000;
    
    full_name     | salary
    --------|---------
    David Austin      | 4800.00
    Valli Pataballa   | 4800.00
    Diana Lorentz     | 4200.00
    Alexander Khoo    | 3100.00
    Shelli Baida      | 2900.00
    Sigal Tobias      | 2800.00
    Guy Himuro        | 2600.00
    Karen Colmenares  | 2500.00
    Kevin Mourgos     | 5800.00
    Julia Nayer       | 3200.00
    Irene Mikkilineni | 2700.00
    James Landry      | 2400.00
    Steven Markle     | 2200.00
    Laura Bissot      | 3300.00
    Mozhe Atkinson    | 2800.00
    James Marlow      | 2500.00
    TJ Olson          | 2100.00
    Jason Mallin      | 3300.00
    Michael Rogers    | 2900.00
    Ki Gee            | 2400.00
    Hazel Philtanker  | 2200.00
    Renske Ladwig     | 3600.00
    Stephen Stiles    | 3200.00
    John Seo          | 2700.00
    Joshua Patel      | 2500.00
    Trenna Rajs       | 3500.00
    Curtis Davies     | 3100.00
    Randall Matos     | 2600.00
    Peter Vargas      | 2500.00
    Winston Taylor    | 3200.00
    Jean Fleaur       | 3100.00
    Martha Sullivan   | 2500.00
    Girard Geoni      | 2800.00
    Nandita Sarchand  | 4200.00
    Alexis Bull       | 4100.00
    Julia Dellinger   | 3400.00
    Anthony Cabrio    | 3000.00
    Kelly Chung       | 3800.00
    Jennifer Dilly    | 3600.00
    Timothy Gates     | 2900.00
    Randall Perkins   | 2500.00
    Sarah Bell        | 4000.00
    Britney Everett   | 3900.00
    Samuel McCain     | 3200.00
    Vance Jones       | 2800.00
    Alana Walsh       | 3100.00
    Kevin Feeney      | 3000.00
    Donald OConnell   | 2600.00
    Douglas Grant     | 2600.00
    Jennifer Whalen   | 4400.00

___
2. Write a query in SQL to display the first and last_name, department number and salary for those employees who earn more than 8000.  
   
    **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**   

        SELECT first_name,last_name, department_id, salary  
            FROM employees
            WHERE salary > 8000;

    first_name | last_name  | department_id |  salary
    ------------|------------|---------------|----------
    Steven     | King       |            90 | 24000.00
    Neena      | Kochhar    |            90 | 17000.00
    Lex        | De Haan    |            90 | 17000.00
    Alexander  | Hunold     |            60 |  9000.00
    Nancy      | Greenberg  |           100 | 12000.00
    Daniel     | Faviet     |           100 |  9000.00
    John       | Chen       |           100 |  8200.00
    Den        | Raphaely   |            30 | 11000.00
    Adam       | Fripp      |            50 |  8200.00
    John       | Russell    |            80 | 14000.00
    Karen      | Partners   |            80 | 13500.00
    Alberto    | Errazuriz  |            80 | 12000.00
    Gerald     | Cambrault  |            80 | 11000.00
    Eleni      | Zlotkey    |            80 | 10500.00
    Peter      | Tucker     |            80 | 10000.00
    David      | Bernstein  |            80 |  9500.00
    Peter      | Hall       |            80 |  9000.00
    Janette    | King       |            80 | 10000.00
    Patrick    | Sully      |            80 |  9500.00
    Allan      | McEwen     |            80 |  9000.00
    Clara      | Vishney    |            80 | 10500.00
    Danielle   | Greene     |            80 |  9500.00
    Lisa       | Ozer       |            80 | 11500.00
    Harrison   | Bloom      |            80 | 10000.00
    Tayler     | Fox        |            80 |  9600.00
    Ellen      | Abel       |            80 | 11000.00
    Alyssa     | Hutton     |            80 |  8800.00
    Jonathon   | Taylor     |            80 |  8600.00
    Jack       | Livingston |            80 |  8400.00
    Michael    | Hartstein  |            20 | 13000.00
    Hermann    | Baer       |            70 | 10000.00
    Shelley    | Higgins    |           110 | 12000.00
    William    | Gietz      |           110 |  8300.00

___
3. Write a query in SQL to display the first and last name, and department number for all employees whose last name is “McEwen”.  

    **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer** 
            
        SELECT first_name, last_name, department_id
        FROM employees
        WHERE last_name = 'McEwen';

    first_name | last_name | department_id
    ------------|-----------|---------------
    Allan      | McEwen    |            80  

___

4. Write a query in SQL to display all the information for all employees without any department number.  

    **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer** 

        SELECT *
        FROM employees
        WHERE department_id IS NULL;

    employee_id | first_name | last_name | email | phone_number | hire_date | job_id | salary | commission_pct | manager_id | department_id
    -------------|------------|-----------|-------|--------------|-----------|--------|--------|----------------|------------|-------------
    (0 rows)

___
5. Write a query in SQL to display all the information about the department Marketing.  

    **database table**: departments

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer** 

        SELECT *
        FROM  departments
        WHERE department_name = 'Marketing';
        

    department_id | department_name | manager_id | location_id
    ---------|--------|------|---------
    20 | Marketing       |        201 |        1800

___
6. Write a query in SQL to display the full name (first and last), hire date, salary, and department number for those employees whose first name does not containing the letter M and make the result set in ascending order by department number.  

    **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer** 

        SELECT first_name || ' ' || last_name as Full_Name,   
        hire_date, salary, department_id
            FROM employees
            WHERE first_name NOT LIKE '%M%'
            ORDER BY department_id;

    full_name     | hire_date  |  salary  | department_id
    -----|---|----|--------
    Kimberely Grant   | 2007-05-24 |  7000.00 |             0
    Jennifer Whalen   | 2003-09-17 |  4400.00 |            10
    Pat Fay           | 2005-08-17 |  6000.00 |            20
    Guy Himuro        | 2006-11-15 |  2600.00 |            30
    Alexander Khoo    | 2003-05-18 |  3100.00 |            30
    Den Raphaely      | 2002-12-07 | 11000.00 |            30
    Shelli Baida      | 2005-12-24 |  2900.00 |            30
    Karen Colmenares  | 2007-08-10 |  2500.00 |            30
    Sigal Tobias      | 2005-07-24 |  2800.00 |            30
    Susan Mavris      | 2002-06-07 |  6500.00 |            40
    Laura Bissot      | 2005-08-20 |  3300.00 |            50
    James Marlow      | 2005-02-16 |  2500.00 |            50
    TJ Olson          | 2007-04-10 |  2100.00 |            50
    Jason Mallin      | 2004-06-14 |  3300.00 |            50
    Ki Gee            | 2007-12-12 |  2400.00 |            50
    Hazel Philtanker  | 2008-02-06 |  2200.00 |            50
    Winston Taylor    | 2006-01-24 |  3200.00 |            50
    Jean Fleaur       | 2006-02-23 |  3100.00 |            50
    Girard Geoni      | 2008-02-03 |  2800.00 |            50
    Nandita Sarchand  | 2004-01-27 |  4200.00 |            50
    Alexis Bull       | 2005-02-20 |  4100.00 |            50
    Julia Dellinger   | 2006-06-24 |  3400.00 |            50
    Anthony Cabrio    | 2007-02-07 |  3000.00 |            50
    Kelly Chung       | 2005-06-14 |  3800.00 |            50
    Jennifer Dilly    | 2005-08-13 |  3600.00 |            50
    Timothy Gates     | 2006-07-11 |  2900.00 |            50
    Randall Perkins   | 2007-12-19 |  2500.00 |            50
    Sarah Bell        | 2004-02-04 |  4000.00 |            50
    Britney Everett   | 2005-03-03 |  3900.00 |            50
    Samuel McCain     | 2006-07-01 |  3200.00 |            50
    Vance Jones       | 2007-03-17 |  2800.00 |            50
    Renske Ladwig     | 2003-07-14 |  3600.00 |            50
    Stephen Stiles    | 2005-10-26 |  3200.00 |            50
    Joshua Patel      | 2006-04-06 |  2500.00 |            50
    Trenna Rajs       | 2003-10-17 |  3500.00 |            50
    Curtis Davies     | 2005-01-29 |  3100.00 |            50
    Randall Matos     | 2006-03-15 |  2600.00 |            50
    Peter Vargas      | 2006-07-09 |  2500.00 |            50
    John Seo          | 2006-02-12 |  2700.00 |            50
    Adam Fripp        | 2005-04-10 |  8200.00 |            50
    Payam Kaufling    | 2003-05-01 |  7900.00 |            50
    Shanta Vollman    | 2005-10-10 |  6500.00 |            50
    Alana Walsh       | 2006-04-24 |  3100.00 |            50
    Kevin Mourgos     | 2007-11-16 |  5800.00 |            50
    Julia Nayer       | 2005-07-16 |  3200.00 |            50
    Irene Mikkilineni | 2006-09-28 |  2700.00 |            50
    James Landry      | 2007-01-14 |  2400.00 |            50
    Steven Markle     | 2008-03-08 |  2200.00 |            50
    Douglas Grant     | 2008-01-13 |  2600.00 |            50
    Donald OConnell   | 2007-06-21 |  2600.00 |            50
    Kevin Feeney      | 2006-05-23 |  3000.00 |            50
    Alexander Hunold  | 2006-01-03 |  9000.00 |            60
    David Austin      | 2005-06-25 |  4800.00 |            60
    Diana Lorentz     | 2007-02-07 |  4200.00 |            60
    Valli Pataballa   | 2006-02-05 |  4800.00 |            60
    Bruce Ernst       | 2007-05-21 |  6000.00 |            60
    Hermann Baer      | 2002-06-07 | 10000.00 |            70
    Amit Banda        | 2008-04-21 |  6200.00 |            80
    John Russell      | 2004-10-01 | 14000.00 |            80
    Karen Partners    | 2005-01-05 | 13500.00 |            80
    Alberto Errazuriz | 2005-03-10 | 12000.00 |            80
    Gerald Cambrault  | 2007-10-15 | 11000.00 |            80
    Eleni Zlotkey     | 2008-01-29 | 10500.00 |            80
    Peter Tucker      | 2005-01-30 | 10000.00 |            80
    David Bernstein   | 2005-03-24 |  9500.00 |            80
    Peter Hall        | 2005-08-20 |  9000.00 |            80
    Christopher Olsen | 2006-03-30 |  8000.00 |            80
    Nanette Cambrault | 2006-12-09 |  7500.00 |            80
    Oliver Tuvault    | 2007-11-23 |  7000.00 |            80
    Janette King      | 2004-01-30 | 10000.00 |            80
    Patrick Sully     | 2004-03-04 |  9500.00 |            80
    Allan McEwen      | 2004-08-01 |  9000.00 |            80
    Lindsey Smith     | 2005-03-10 |  8000.00 |            80
    Louise Doran      | 2005-12-15 |  7500.00 |            80
    Sarath Sewall     | 2006-11-03 |  7000.00 |            80
    Clara Vishney     | 2005-11-11 | 10500.00 |            80
    Danielle Greene   | 2007-03-19 |  9500.00 |            80
    David Lee         | 2008-02-23 |  6800.00 |            80
    Sundar Ande       | 2008-03-24 |  6400.00 |            80
    Lisa Ozer         | 2005-03-11 | 11500.00 |            80
    Harrison Bloom    | 2006-03-23 | 10000.00 |            80
    Tayler Fox        | 2006-01-24 |  9600.00 |            80
    William Smith     | 2007-02-23 |  7400.00 |            80
    Elizabeth Bates   | 2007-03-24 |  7300.00 |            80
    Sundita Kumar     | 2008-04-21 |  6100.00 |            80
    Ellen Abel        | 2004-05-11 | 11000.00 |            80
    Alyssa Hutton     | 2005-03-19 |  8800.00 |            80
    Jonathon Taylor   | 2006-03-24 |  8600.00 |            80
    Jack Livingston   | 2006-04-23 |  8400.00 |            80
    Charles Johnson   | 2008-01-04 |  6200.00 |            80
    Steven King       | 2003-06-17 | 24000.00 |            90
    Lex De Haan       | 2001-01-13 | 17000.00 |            90
    Neena Kochhar     | 2005-09-21 | 17000.00 |            90
    John Chen         | 2005-09-28 |  8200.00 |           100
    Daniel Faviet     | 2002-08-16 |  9000.00 |           100
    Nancy Greenberg   | 2002-08-17 | 12000.00 |           100
    Luis Popp         | 2007-12-07 |  6900.00 |           100
    Ismael Sciarra    | 2005-09-30 |  7700.00 |           100
    Shelley Higgins   | 2002-06-07 | 12000.00 |           110
    William Gietz     | 2002-06-07 |  8300.00 |           110


___
7. Write a query in SQL to display all the information of employees whose salary is in the range of 8000 and 12000 and commission is not null or department number is except the number 40, 120 and 70 and they have been hired before June 5th, 1987. 

    **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer** 

        SELECT *
        FROM employees
        WHERE salary BETWEEN 8000 AND 12000 
            AND commission_pct IS NOT NULL
            OR department_id NOT IN (40 , 120 , 70)
            AND hire_date < '1987-06-05'
    
    employee_id | first_name  | last_name  |  email   |    phone_number    | hire_date  |   job_id   |  salary  | commission_pct | manager_id | department_id
    ---|---|-----|-----|----|-----|----|---|----|----|---
    103 | Alexander   | Hunold     | AHUNOLD  | 590.423.4567       | 2006-01-03 | IT_PROG    |  9000.00 |           0.00 |      102 |            60
    108 | Nancy       | Greenberg  | NGREENBE | 515.124.4569       | 2002-08-17 | FI_MGR     | 12000.00 |           0.00 |      101 |           100
    109 | Daniel      | Faviet     | DFAVIET  | 515.124.4169       | 2002-08-16 | FI_ACCOUNT |  9000.00 |           0.00 |      108 |           100
    110 | John        | Chen       | JCHEN    | 515.124.4269       | 2005-09-28 | FI_ACCOUNT |  8200.00 |           0.00 |      108 |           100
    114 | Den         | Raphaely   | DRAPHEAL | 515.127.4561       | 2002-12-07 | PU_MAN     | 11000.00 |           0.00 |      100 |            30
    120 | Matthew     | Weiss      | MWEISS   | 650.123.1234       | 2004-07-18 | ST_MAN     |  8000.00 |           0.00 |      100 |            50
    121 | Adam        | Fripp      | AFRIPP   | 650.123.2234       | 2005-04-10 | ST_MAN     |  8200.00 |           0.00 |      100 |            50
    147 | Alberto     | Errazuriz  | AERRAZUR | 011.44.1344.429278 | 2005-03-10 | SA_MAN     | 12000.00 |           0.30 |      100 |            80
    148 | Gerald      | Cambrault  | GCAMBRAU | 011.44.1344.619268 | 2007-10-15 | SA_MAN     | 11000.00 |           0.30 |      100 |            80
    149 | Eleni       | Zlotkey    | EZLOTKEY | 011.44.1344.429018 | 2008-01-29 | SA_MAN     | 10500.00 |           0.20 |      100 |            80
    150 | Peter       | Tucker     | PTUCKER  | 011.44.1344.129268 | 2005-01-30 | SA_REP     | 10000.00 |           0.30 |      145 |            80
    151 | David       | Bernstein  | DBERNSTE | 011.44.1344.345268 | 2005-03-24 | SA_REP     |  9500.00 |           0.25 |      145 |            80
    152 | Peter       | Hall       | PHALL    | 011.44.1344.478968 | 2005-08-20 | SA_REP     |  9000.00 |           0.25 |      145 |            80
    153 | Christopher | Olsen      | COLSEN   | 011.44.1344.498718 | 2006-03-30 | SA_REP     |  8000.00 |           0.20 |      145 |            80
    156 | Janette     | King       | JKING    | 011.44.1345.429268 | 2004-01-30 | SA_REP     | 10000.00 |           0.35 |      146 |            80
    157 | Patrick     | Sully      | PSULLY   | 011.44.1345.929268 | 2004-03-04 | SA_REP     |  9500.00 |           0.35 |      146 |            80
    158 | Allan       | McEwen     | AMCEWEN  | 011.44.1345.829268 | 2004-08-01 | SA_REP     |  9000.00 |           0.35 |      146 |            80
    159 | Lindsey     | Smith      | LSMITH   | 011.44.1345.729268 | 2005-03-10 | SA_REP     |  8000.00 |           0.30 |      146 |            80
    162 | Clara       | Vishney    | CVISHNEY | 011.44.1346.129268 | 2005-11-11 | SA_REP     | 10500.00 |           0.25 |      147 |            80
    163 | Danielle    | Greene     | DGREENE  | 011.44.1346.229268 | 2007-03-19 | SA_REP     |  9500.00 |           0.15 |      147 |            80
    168 | Lisa        | Ozer       | LOZER    | 011.44.1343.929268 | 2005-03-11 | SA_REP     | 11500.00 |           0.25 |      148 |            80
    169 | Harrison    | Bloom      | HBLOOM   | 011.44.1343.829268 | 2006-03-23 | SA_REP     | 10000.00 |           0.20 |      148 |            80
    170 | Tayler      | Fox        | TFOX     | 011.44.1343.729268 | 2006-01-24 | SA_REP     |  9600.00 |           0.20 |      148 |            80
    174 | Ellen       | Abel       | EABEL    | 011.44.1644.429267 | 2004-05-11 | SA_REP     | 11000.00 |           0.30 |      149 |            80
    175 | Alyssa      | Hutton     | AHUTTON  | 011.44.1644.429266 | 2005-03-19 | SA_REP     |  8800.00 |           0.25 |      149 |            80
    176 | Jonathon    | Taylor     | JTAYLOR  | 011.44.1644.429265 | 2006-03-24 | SA_REP     |  8600.00 |           0.20 |      149 |            80
    177 | Jack        | Livingston | JLIVINGS | 011.44.1644.429264 | 2006-04-23 | SA_REP     |  8400.00 |           0.20 |      149 |            80
    204 | Hermann     | Baer       | HBAER    | 515.123.8888       | 2002-06-07 | PR_REP     | 10000.00 |           0.00 |      101 |            70
    205 | Shelley     | Higgins    | SHIGGINS | 515.123.8080       | 2002-06-07 | AC_MGR     | 12000.00 |           0.00 |      101 |           110
    206 | William     | Gietz      | WGIETZ   | 515.123.8181       | 2002-06-07 | AC_ACCOUNT |  8300.00 |           0.00 |      205 |           110


___
8. Write a query in SQL to display the full name (first and last name), and salary for all employees who does not earn any commission.  

    **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer** 

        SELECT first_name ||' '||last_name AS Full_Name, salary  
        FROM  employees
        WHERE commission_pct IS NULL;

    full_name | salary
    ----|--------
      (0 rows)

___
9. Write a query in SQL to display the full name (first and last), the phone number and email separated by hyphen, and salary, for those employees whose salary is within the range of 9000 and 17000. The column headings assign with Full_Name, Contact_Details and Remuneration respectively.  

    **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer** 

        SELECT first_name ||' '||last_name AS Full_Name,  
        phone_number ||' - '|| email AS Contact_Details,  
        salary  AS Remuneration  
            FROM employees  
            WHERE salary 
            BETWEEN 9000 AND 17000;  

    full_name     |        contact_details        | remuneration
    ---|-------|-------------
    Neena Kochhar     | 515.123.4568 - NKOCHHAR       |     17000.00
    Lex De Haan       | 515.123.4569 - LDEHAAN        |     17000.00
    Alexander Hunold  | 590.423.4567 - AHUNOLD        |      9000.00
    Nancy Greenberg   | 515.124.4569 - NGREENBE       |     12000.00
    Daniel Faviet     | 515.124.4169 - DFAVIET        |      9000.00
    Den Raphaely      | 515.127.4561 - DRAPHEAL       |     11000.00
    John Russell      | 011.44.1344.429268 - JRUSSEL  |     14000.00
    Karen Partners    | 011.44.1344.467268 - KPARTNER |     13500.00
    Alberto Errazuriz | 011.44.1344.429278 - AERRAZUR |     12000.00
    Gerald Cambrault  | 011.44.1344.619268 - GCAMBRAU |     11000.00
    Eleni Zlotkey     | 011.44.1344.429018 - EZLOTKEY |     10500.00
    Peter Tucker      | 011.44.1344.129268 - PTUCKER  |     10000.00
    David Bernstein   | 011.44.1344.345268 - DBERNSTE |      9500.00
    Peter Hall        | 011.44.1344.478968 - PHALL    |      9000.00
    Janette King      | 011.44.1345.429268 - JKING    |     10000.00
    Patrick Sully     | 011.44.1345.929268 - PSULLY   |      9500.00
    Allan McEwen      | 011.44.1345.829268 - AMCEWEN  |      9000.00
    Clara Vishney     | 011.44.1346.129268 - CVISHNEY |     10500.00
    Danielle Greene   | 011.44.1346.229268 - DGREENE  |      9500.00
    Lisa Ozer         | 011.44.1343.929268 - LOZER    |     11500.00
    Harrison Bloom    | 011.44.1343.829268 - HBLOOM   |     10000.00
    Tayler Fox        | 011.44.1343.729268 - TFOX     |      9600.00
    Ellen Abel        | 011.44.1644.429267 - EABEL    |     11000.00
    Michael Hartstein | 515.123.5555 - MHARTSTE       |     13000.00
    Hermann Baer      | 515.123.8888 - HBAER          |     10000.00
    Shelley Higgins   | 515.123.8080 - SHIGGINS       |     12000.00

___
10. Write a query in SQL to display the first and last name, and salary for those employees whose first name is ending with the letter m.  

    **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer** 

        SELECT first_name, last_name, salary
        FROM employees
        WHERE first_name LIKE '%m';

    first_name | last_name | salary
    ---|----|---------
    Adam       | Fripp     | 8200.00
    Payam      | Kaufling  | 7900.00
    William    | Smith     | 7400.00
    William    | Gietz     | 8300.00

___
11. Write a query in SQL to display the full name (first and last) name, and salary, for all employees whose salary is out of the range 7000 and 15000 and make the result set in ascending order by the full name.  

     **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer** 

        SELECT first_name || ' ' || last_name as Name, salary
        FROM  employees
        WHERE salary NOT BETWEEN 7000 AND 15000
            ORDER BY first_name || ' ' || last_name;


    name        |  salary
    -----|---------
    Alana Walsh       |  3100.00
    Alexander Khoo    |  3100.00
    Alexis Bull       |  4100.00
    Amit Banda        |  6200.00
    Anthony Cabrio    |  3000.00
    Britney Everett   |  3900.00
    Bruce Ernst       |  6000.00
    Charles Johnson   |  6200.00
    Curtis Davies     |  3100.00
    David Austin      |  4800.00
    David Lee         |  6800.00
    Diana Lorentz     |  4200.00
    Donald OConnell   |  2600.00
    Douglas Grant     |  2600.00
    Girard Geoni      |  2800.00
    Guy Himuro        |  2600.00
    Hazel Philtanker  |  2200.00
    Irene Mikkilineni |  2700.00
    James Landry      |  2400.00
    James Marlow      |  2500.00
    Jason Mallin      |  3300.00
    Jean Fleaur       |  3100.00
    Jennifer Dilly    |  3600.00
    Jennifer Whalen   |  4400.00
    John Seo          |  2700.00
    Joshua Patel      |  2500.00
    Julia Dellinger   |  3400.00
    Julia Nayer       |  3200.00
    Karen Colmenares  |  2500.00
    Kelly Chung       |  3800.00
    Kevin Feeney      |  3000.00
    Kevin Mourgos     |  5800.00
    Ki Gee            |  2400.00
    Laura Bissot      |  3300.00
    Lex De Haan       | 17000.00
    Luis Popp         |  6900.00
    Martha Sullivan   |  2500.00
    Michael Rogers    |  2900.00
    Mozhe Atkinson    |  2800.00
    Nandita Sarchand  |  4200.00
    Neena Kochhar     | 17000.00
    Pat Fay           |  6000.00
    Peter Vargas      |  2500.00
    Randall Matos     |  2600.00
    Randall Perkins   |  2500.00
    Renske Ladwig     |  3600.00
    Samuel McCain     |  3200.00
    Sarah Bell        |  4000.00
    Shanta Vollman    |  6500.00
    Shelli Baida      |  2900.00
    Sigal Tobias      |  2800.00
    Stephen Stiles    |  3200.00
    Steven King       | 24000.00
    Steven Markle     |  2200.00
    Sundar Ande       |  6400.00
    Sundita Kumar     |  6100.00
    Susan Mavris      |  6500.00
    Timothy Gates     |  2900.00
    TJ Olson          |  2100.00
    Trenna Rajs       |  3500.00
    Valli Pataballa   |  4800.00
    Vance Jones       |  2800.00
    Winston Taylor    |  3200.00
        
___
12. Write a query in SQL to display the full name (first and last), job id and date of hire for those employees who was hired during November 5th, 2007 and July 5th, 2009. 

    **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer** 

        SELECT first_name ||' '||last_name AS Full_Name, 
        job_id, hire_date 
        FROM employees 
            WHERE hire_date 
            BETWEEN '2007-11-05' AND '2009-07-05';

    full_name     |   job_id   | hire_date
    ------|------|------
    Luis Popp        | FI_ACCOUNT | 2007-12-07
    Kevin Mourgos    | ST_MAN     | 2007-11-16
    Steven Markle    | ST_CLERK   | 2008-03-08
    Ki Gee           | ST_CLERK   | 2007-12-12
    Hazel Philtanker | ST_CLERK   | 2008-02-06
    Eleni Zlotkey    | SA_MAN     | 2008-01-29
    Oliver Tuvault   | SA_REP     | 2007-11-23
    Mattea Marvins   | SA_REP     | 2008-01-24
    David Lee        | SA_REP     | 2008-02-23
    Sundar Ande      | SA_REP     | 2008-03-24
    Amit Banda       | SA_REP     | 2008-04-21
    Sundita Kumar    | SA_REP     | 2008-04-21
    Charles Johnson  | SA_REP     | 2008-01-04
    Girard Geoni     | SH_CLERK   | 2008-02-03
    Randall Perkins  | SH_CLERK   | 2007-12-19
    Douglas Grant    | SH_CLERK   | 2008-01-13

___
13. Write a query in SQL to display the the full name (first and last name), and department number for those employees who works either in department 70 or 90.  

    **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer** 

        SELECT first_name ||' '|| last_name AS Full_Name, department_id  
        FROM employees
        WHERE department_id IN (70 , 90);
        
    full_name   | department_id
    ---|--------
    Steven King   |            90
    Neena Kochhar |            90
    Lex De Haan   |            90
    Hermann Baer  |            70

___
14. Write a query in SQL to display the full name (first and last name), salary, and manager number for those employees who is working under a manager.  

    **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer** 

        SELECT first_name ||' '||last_name AS Full_Name,  
        salary, manager_id
            FROM employees
            WHERE manager_id IS NOT NULL;


    full_name     |  salary  | manager_id
    -------|-----|------
    Neena Kochhar     | 17000.00 |        100
    Lex De Haan       | 17000.00 |        100
    Alexander Hunold  |  9000.00 |        102
    Bruce Ernst       |  6000.00 |        103
    David Austin      |  4800.00 |        103
    Valli Pataballa   |  4800.00 |        103
    Diana Lorentz     |  4200.00 |        103
    Nancy Greenberg   | 12000.00 |        101
    Daniel Faviet     |  9000.00 |        108
    John Chen         |  8200.00 |        108
    Ismael Sciarra    |  7700.00 |        108
    Jose Manuel Urman |  7800.00 |        108
    Luis Popp         |  6900.00 |        108
    Den Raphaely      | 11000.00 |        100
    Alexander Khoo    |  3100.00 |        114
    Shelli Baida      |  2900.00 |        114
    Sigal Tobias      |  2800.00 |        114
    Guy Himuro        |  2600.00 |        114
    Karen Colmenares  |  2500.00 |        114
    Matthew Weiss     |  8000.00 |        100
    Adam Fripp        |  8200.00 |        100
    Payam Kaufling    |  7900.00 |        100
    Shanta Vollman    |  6500.00 |        100
    Kevin Mourgos     |  5800.00 |        100
    Julia Nayer       |  3200.00 |        120
    Irene Mikkilineni |  2700.00 |        120
    James Landry      |  2400.00 |        120
    Steven Markle     |  2200.00 |        120
    Laura Bissot      |  3300.00 |        121
    Mozhe Atkinson    |  2800.00 |        121
    James Marlow      |  2500.00 |        121
    TJ Olson          |  2100.00 |        121
    Jason Mallin      |  3300.00 |        122
    Michael Rogers    |  2900.00 |        122
    Ki Gee            |  2400.00 |        122
    Hazel Philtanker  |  2200.00 |        122
    Renske Ladwig     |  3600.00 |        123
    Stephen Stiles    |  3200.00 |        123
    John Seo          |  2700.00 |        123
    Joshua Patel      |  2500.00 |        123
    Trenna Rajs       |  3500.00 |        124
    Curtis Davies     |  3100.00 |        124
    Randall Matos     |  2600.00 |        124
    Peter Vargas      |  2500.00 |        124
    John Russell      | 14000.00 |        100
    Karen Partners    | 13500.00 |        100
    Alberto Errazuriz | 12000.00 |        100
    Gerald Cambrault  | 11000.00 |        100
    Eleni Zlotkey     | 10500.00 |        100
    Peter Tucker      | 10000.00 |        145
    David Bernstein   |  9500.00 |        145
    Peter Hall        |  9000.00 |        145
    Christopher Olsen |  8000.00 |        145
    Nanette Cambrault |  7500.00 |        145
    Oliver Tuvault    |  7000.00 |        145
    Janette King      | 10000.00 |        146
    Patrick Sully     |  9500.00 |        146
    Allan McEwen      |  9000.00 |        146
    Lindsey Smith     |  8000.00 |        146
    Louise Doran      |  7500.00 |        146
    Sarath Sewall     |  7000.00 |        146
    Clara Vishney     | 10500.00 |        147
    Danielle Greene   |  9500.00 |        147
    Mattea Marvins    |  7200.00 |        147
    David Lee         |  6800.00 |        147
    Sundar Ande       |  6400.00 |        147
    Amit Banda        |  6200.00 |        147
    Lisa Ozer         | 11500.00 |        148
    Harrison Bloom    | 10000.00 |        148
    Tayler Fox        |  9600.00 |        148
    William Smith     |  7400.00 |        148
    Elizabeth Bates   |  7300.00 |        148
    Sundita Kumar     |  6100.00 |        148
    Ellen Abel        | 11000.00 |        149
    Alyssa Hutton     |  8800.00 |        149
    Jonathon Taylor   |  8600.00 |        149
    Jack Livingston   |  8400.00 |        149
    Kimberely Grant   |  7000.00 |        149
    Charles Johnson   |  6200.00 |        149
    Winston Taylor    |  3200.00 |        120
    Jean Fleaur       |  3100.00 |        120
    Martha Sullivan   |  2500.00 |        120
    Girard Geoni      |  2800.00 |        120
    Nandita Sarchand  |  4200.00 |        121
    Alexis Bull       |  4100.00 |        121
    Julia Dellinger   |  3400.00 |        121
    Anthony Cabrio    |  3000.00 |        121
    Kelly Chung       |  3800.00 |        122
    Jennifer Dilly    |  3600.00 |        122
    Timothy Gates     |  2900.00 |        122
    Randall Perkins   |  2500.00 |        122
    Sarah Bell        |  4000.00 |        123
    Britney Everett   |  3900.00 |        123
    Samuel McCain     |  3200.00 |        123
    Vance Jones       |  2800.00 |        123
    Alana Walsh       |  3100.00 |        124
    Kevin Feeney      |  3000.00 |        124
    Donald OConnell   |  2600.00 |        124
    Douglas Grant     |  2600.00 |        124
    Jennifer Whalen   |  4400.00 |        101
    Michael Hartstein | 13000.00 |        100
    Pat Fay           |  6000.00 |        201
    Susan Mavris      |  6500.00 |        101
    Hermann Baer      | 10000.00 |        101
    Shelley Higgins   | 12000.00 |        101
    William Gietz     |  8300.00 |        205
___
15. Write a query in SQL to display all the information from Employees table for those employees who was hired before June 21st, 2002.  

    **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer** 

        SELECT *
        FROM employees
        WHERE hire_date < '2002-06-21';

    employee_id |first_name | last_name | email| phone_number | hire_date  |job_id| salary| commission_pct | manager_id | department_id
    ---|-------|-----|-----|----|------|-----|----|-----|----|-----
    102 | Lex        | De Haan   | LDEHAAN  | 515.123.4569 | 2001-01-13 | AD_VP      | 17000.00 |           0.00 |        100 |            90
    203 | Susan      | Mavris    | SMAVRIS  | 515.123.7777 | 2002-06-07 | HR_REP     |  6500.00 |           0.00 |        101 |            40
    204 | Hermann    | Baer      | HBAER    | 515.123.8888 | 2002-06-07 | PR_REP     | 10000.00 |           0.00 |        101 |            70
    205 | Shelley    | Higgins   | SHIGGINS | 515.123.8080 | 2002-06-07 | AC_MGR     | 12000.00 |           0.00 |        101 |           110
    206 | William    | Gietz     | WGIETZ   | 515.123.8181 | 2002-06-07 | AC_ACCOUNT |  8300.00 |           0.00 |        205 |           110

___
16. Write a query in SQL to display the first and last name, email, salary and manager ID, for those employees whose managers are hold the ID 120, 103 or 145.  

    **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer** 

        SELECT first_name, last_name, email, 
        salary, manager_id
            FROM employees
            WHERE manager_id IN (120 , 103 , 145);

    first_name  |  last_name  |  email   |  salary  | manager_id
    -----|------|-----|-----|-----
    Bruce       | Ernst       | BERNST   |  6000.00 |        103
    David       | Austin      | DAUSTIN  |  4800.00 |        103
    Valli       | Pataballa   | VPATABAL |  4800.00 |        103
    Diana       | Lorentz     | DLORENTZ |  4200.00 |        103
    Julia       | Nayer       | JNAYER   |  3200.00 |        120
    Irene       | Mikkilineni | IMIKKILI |  2700.00 |        120
    James       | Landry      | JLANDRY  |  2400.00 |        120
    Steven      | Markle      | SMARKLE  |  2200.00 |        120
    Peter       | Tucker      | PTUCKER  | 10000.00 |        145
    David       | Bernstein   | DBERNSTE |  9500.00 |        145
    Peter       | Hall        | PHALL    |  9000.00 |        145
    Christopher | Olsen       | COLSEN   |  8000.00 |        145
    Nanette     | Cambrault   | NCAMBRAU |  7500.00 |        145
    Oliver      | Tuvault     | OTUVAULT |  7000.00 |        145
    Winston     | Taylor      | WTAYLOR  |  3200.00 |        120
    Jean        | Fleaur      | JFLEAUR  |  3100.00 |        120
    Martha      | Sullivan    | MSULLIVA |  2500.00 |        120
    Girard      | Geoni       | GGEONI   |  2800.00 |        120

___
17. Write a query in SQL to display all the information for all employees who have the letters D, S, or N in their first name and also arrange the result in descending order by salary.  

    **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer** 

        SELECT *
        FROM employees
        WHERE first_name LIKE '%D%'
        OR first_name LIKE '%S%'
        OR first_name LIKE '%N%'
            ORDER BY salary DESC;
    
    employee_id | first_name | last_name |  email   |    phone_number    | hire_date  |   job_id   |  salary  | commission_pct | manager_id | department_id
    --------|-------|------|----|------|----|-----|----|-----|----|----
    100 | Steven     | King      | SKING    | 515.123.4567       | 2003-06-17 | AD_PRES    | 24000.00 |           0.00 |          0 |            90
    101 | Neena      | Kochhar   | NKOCHHAR | 515.123.4568       | 2005-09-21 | AD_VP      | 17000.00 |           0.00 |        100 |            90
    205 | Shelley    | Higgins   | SHIGGINS | 515.123.8080       | 2002-06-07 | AC_MGR     | 12000.00 |           0.00 |        101 |           110
    108 | Nancy      | Greenberg | NGREENBE | 515.124.4569       | 2002-08-17 | FI_MGR     | 12000.00 |           0.00 |        101 |           100
    114 | Den        | Raphaely  | DRAPHEAL | 515.127.4561       | 2002-12-07 | PU_MAN     | 11000.00 |           0.00 |        100 |            30
    151 | David      | Bernstein | DBERNSTE | 011.44.1344.345268 | 2005-03-24 | SA_REP     |  9500.00 |           0.25 |        145 |            80
    163 | Danielle   | Greene    | DGREENE  | 011.44.1346.229268 | 2007-03-19 | SA_REP     |  9500.00 |           0.15 |        147 |            80
    109 | Daniel     | Faviet    | DFAVIET  | 515.124.4169       | 2002-08-16 | FI_ACCOUNT |  9000.00 |           0.00 |        108 |           100
    154 | Nanette    | Cambrault | NCAMBRAU | 011.44.1344.987668 | 2006-12-09 | SA_REP     |  7500.00 |           0.20 |        145 |            80
    161 | Sarath     | Sewall    | SSEWALL  | 011.44.1345.529268 | 2006-11-03 | SA_REP     |  7000.00 |           0.25 |        146 |            80
    165 | David      | Lee       | DLEE     | 011.44.1346.529268 | 2008-02-23 | SA_REP     |  6800.00 |           0.10 |        147 |            80
    123 | Shanta     | Vollman   | SVOLLMAN | 650.123.4234       | 2005-10-10 | ST_MAN     |  6500.00 |           0.00 |        100 |            50
    203 | Susan      | Mavris    | SMAVRIS  | 515.123.7777       | 2002-06-07 | HR_REP     |  6500.00 |           0.00 |        101 |            40
    166 | Sundar     | Ande      | SANDE    | 011.44.1346.629268 | 2008-03-24 | SA_REP     |  6400.00 |           0.10 |        147 |            80
    173 | Sundita    | Kumar     | SKUMAR   | 011.44.1343.329268 | 2008-04-21 | SA_REP     |  6100.00 |           0.10 |        148 |            80
    105 | David      | Austin    | DAUSTIN  | 590.423.4569       | 2005-06-25 | IT_PROG    |  4800.00 |           0.00 |        103 |            60
    184 | Nandita    | Sarchand  | NSARCHAN | 650.509.1876       | 2004-01-27 | SH_CLERK   |  4200.00 |           0.00 |        121 |            50
    107 | Diana      | Lorentz   | DLORENTZ | 590.423.5567       | 2007-02-07 | IT_PROG    |  4200.00 |           0.00 |        103 |            60
    192 | Sarah      | Bell      | SBELL    | 650.501.1876       | 2004-02-04 | SH_CLERK   |  4000.00 |           0.00 |        123 |            50
    194 | Samuel     | McCain    | SMCCAIN  | 650.501.3876       | 2006-07-01 | SH_CLERK   |  3200.00 |           0.00 |        123 |            50
    138 | Stephen    | Stiles    | SSTILES  | 650.121.2034       | 2005-10-26 | ST_CLERK   |  3200.00 |           0.00 |        123 |            50
    116 | Shelli     | Baida     | SBAIDA   | 515.127.4563       | 2005-12-24 | PU_CLERK   |  2900.00 |           0.00 |        114 |            30
    117 | Sigal      | Tobias    | STOBIAS  | 515.127.4564       | 2005-07-24 | PU_CLERK   |  2800.00 |           0.00 |        114 |            30
    198 | Donald     | OConnell  | DOCONNEL | 650.507.9833       | 2007-06-21 | SH_CLERK   |  2600.00 |           0.00 |        124 |            50
    199 | Douglas    | Grant     | DGRANT   | 650.507.9844       | 2008-01-13 | SH_CLERK   |  2600.00 |           0.00 |        124 |            50
    128 | Steven     | Markle    | SMARKLE  | 650.124.1434       | 2008-03-08 | ST_CLERK   |  2200.00 |           0.00 |        120 |            50

___
18. Write a query in SQL to display the full name (first name and last name), hire date, commission percentage, email and telephone separated by '-', and salary for those employees who earn the salary above 11000 or the seventh digit in their phone number equals 3 and make the result set in a descending order by the first name.  

    **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer** 

        SELECT first_name ||' '||last_name AS Full_Name,
        hire_date, commission_pct, 
        email ||' -  '||phone_number AS Contact_Details, salary 
            FROM employees 
            WHERE salary > 11000
                OR phone_number LIKE '______3%'
                ORDER BY first_name DESC;

    full_name     | hire_date  | commission_pct |        contact_details         |  salary
    ----------|-------|------|------|-----
    William Gietz     | 2002-06-07 |           0.00 | WGIETZ -  515.123.8181         |  8300.00
    Valli Pataballa   | 2006-02-05 |           0.00 | VPATABAL -  590.423.4560       |  4800.00
    Susan Mavris      | 2002-06-07 |           0.00 | SMAVRIS -  515.123.7777        |  6500.00
    Steven King       | 2003-06-17 |           0.00 | SKING -  515.123.4567          | 24000.00
    Shelley Higgins   | 2002-06-07 |           0.00 | SHIGGINS -  515.123.8080       | 12000.00
    Shanta Vollman    | 2005-10-10 |           0.00 | SVOLLMAN -  650.123.4234       |  6500.00
    Payam Kaufling    | 2003-05-01 |           0.00 | PKAUFLIN -  650.123.3234       |  7900.00
    Pat Fay           | 2005-08-17 |           0.00 | PFAY -  603.123.6666           |  6000.00
    Neena Kochhar     | 2005-09-21 |           0.00 | NKOCHHAR -  515.123.4568       | 17000.00
    Nancy Greenberg   | 2002-08-17 |           0.00 | NGREENBE -  515.124.4569       | 12000.00
    Michael Hartstein | 2004-02-17 |           0.00 | MHARTSTE -  515.123.5555       | 13000.00
    Matthew Weiss     | 2004-07-18 |           0.00 | MWEISS -  650.123.1234         |  8000.00
    Lisa Ozer         | 2005-03-11 |           0.25 | LOZER -  011.44.1343.929268    | 11500.00
    Lex De Haan       | 2001-01-13 |           0.00 | LDEHAAN -  515.123.4569        | 17000.00
    Kevin Mourgos     | 2007-11-16 |           0.00 | KMOURGOS -  650.123.5234       |  5800.00
    Karen Partners    | 2005-01-05 |           0.30 | KPARTNER -  011.44.1344.467268 | 13500.00
    John Russell      | 2004-10-01 |           0.40 | JRUSSEL -  011.44.1344.429268  | 14000.00
    Jennifer Whalen   | 2003-09-17 |           0.00 | JWHALEN -  515.123.4444        |  4400.00
    Hermann Baer      | 2002-06-07 |           0.00 | HBAER -  515.123.8888          | 10000.00
    Diana Lorentz     | 2007-02-07 |           0.00 | DLORENTZ -  590.423.5567       |  4200.00
    David Austin      | 2005-06-25 |           0.00 | DAUSTIN -  590.423.4569        |  4800.00
    Bruce Ernst       | 2007-05-21 |           0.00 | BERNST -  590.423.4568         |  6000.00
    Alexander Hunold  | 2006-01-03 |           0.00 | AHUNOLD -  590.423.4567        |  9000.00
    Alberto Errazuriz | 2005-03-10 |           0.30 | AERRAZUR -  011.44.1344.429278 | 12000.00
    Adam Fripp        | 2005-04-10 |           0.00 | AFRIPP -  650.123.2234         |  8200.00
___
19. Write a query in SQL to display the first and last name, and department number for those employees who holds a letter s as a 3rd character in their first name. 


    **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer** 

        SELECT first_name,last_name, department_id
        FROM employees
        WHERE first_name LIKE '__s%';


    first_name  | last_name | department_id
    ----|----|-----
    Jose Manuel | Urman     |           100
    Jason       | Mallin    |            50
    Joshua      | Patel     |            50
    Lisa        | Ozer      |            80
    Susan       | Mavris    |            40

___
20. Write a query in SQL to display the employee ID, first name, job id, and department number for those employees who is working except the departments 50,30 and 80. 
    
     **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer** 

        SELECT employee_id, first_name, job_id, department_id
        FROM employees
        WHERE department_id NOT IN (50, 30, 80);

    employee_id | first_name  |   job_id   | department_id
    ----|------|-----|-----
    100 | Steven      | AD_PRES    |            90
    101 | Neena       | AD_VP      |            90
    102 | Lex         | AD_VP      |            90
    103 | Alexander   | IT_PROG    |            60
    104 | Bruce       | IT_PROG    |            60
    105 | David       | IT_PROG    |            60
    106 | Valli       | IT_PROG    |            60
    107 | Diana       | IT_PROG    |            60
    108 | Nancy       | FI_MGR     |           100
    109 | Daniel      | FI_ACCOUNT |           100
    110 | John        | FI_ACCOUNT |           100
    111 | Ismael      | FI_ACCOUNT |           100
    112 | Jose Manuel | FI_ACCOUNT |           100
    113 | Luis        | FI_ACCOUNT |           100
    178 | Kimberely   | SA_REP     |             0
    200 | Jennifer    | AD_ASST    |            10
    201 | Michael     | MK_MAN     |            20
    202 | Pat         | MK_REP     |            20
    203 | Susan       | HR_REP     |            40
    204 | Hermann     | PR_REP     |            70
    205 | Shelley     | AC_MGR     |           110
    206 | William     | AC_ACCOUNT |           110

___
21. Write a query in SQL to display the employee Id, first name, job id, and department number for those employees whose department number equals 30, 40 or 90.  
   
    **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer** 

        SELECT employee_id, first_name, job_id, department_id
        FROM employees
        WHERE department_id IN (30 , 40 , 90);

    employee_id | first_name |  job_id  | department_id
    ----|------|-----|----
    100 | Steven     | AD_PRES  |            90
    101 | Neena      | AD_VP    |            90
    102 | Lex        | AD_VP    |            90
    114 | Den        | PU_MAN   |            30
    115 | Alexander  | PU_CLERK |            30
    116 | Shelli     | PU_CLERK |            30
    117 | Sigal      | PU_CLERK |            30
    118 | Guy        | PU_CLERK |            30
    119 | Karen      | PU_CLERK |            30
    203 | Susan      | HR_REP   |            40
___
22. Write a query in SQL to display the ID for those employees who did two or more jobs in the past.  

    **database table**: job_history

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer** 

        SELECT employee_id 
        FROM job_history 
            GROUP BY employee_id 
                HAVING COUNT(*) >= 2;

    employee_id|
    ------|
    101|
    176|
    200|

___
23. Write a query in SQL to display job ID, number of employees, sum of salary, and difference between highest salary and lowest salary for a job.  

    **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer** 

        SELECT job_id, COUNT(*), SUM(salary), 
        MAX(salary)-MIN(salary) AS salary_difference 
            FROM employees 
                GROUP BY job_id;

    job_id   | count |    sum    | salary_difference
    ------|----|----|----
    AC_ACCOUNT |     1 |   8300.00 |              0.00
    ST_MAN     |     5 |  36400.00 |           2400.00
    IT_PROG    |     5 |  28800.00 |           4800.00
    SA_MAN     |     5 |  61000.00 |           3500.00
    AD_PRES    |     1 |  24000.00 |              0.00
    AC_MGR     |     1 |  12000.00 |              0.00
    FI_MGR     |     1 |  12000.00 |              0.00
    AD_ASST    |     1 |   4400.00 |              0.00
    MK_MAN     |     1 |  13000.00 |              0.00
    PU_CLERK   |     5 |  13900.00 |            600.00
    HR_REP     |     1 |   6500.00 |              0.00
    PR_REP     |     1 |  10000.00 |              0.00
    FI_ACCOUNT |     5 |  39600.00 |           2100.00
    SH_CLERK   |    20 |  64300.00 |           1700.00
    AD_VP      |     2 |  34000.00 |              0.00
    SA_REP     |    30 | 250500.00 |           5400.00
    ST_CLERK   |    20 |  55700.00 |           1500.00
    MK_REP     |     1 |   6000.00 |              0.00
    PU_MAN     |     1 |  11000.00 |              0.00

___
24. Write a query in SQL to display job ID for those jobs that were done by two or more for more than 300 days.  

    **database table**: job_history

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer** 

        SELECT job_id 
        FROM job_history 
            WHERE end_date-start_date > 300 
                GROUP BY job_id 
                    HAVING COUNT(*) >= 2;


    job_id|
    -----|
    AC_ACCOUNT|
    ST_CLERK|

___

25. Write a query in SQL to display the country ID and number of cities in that country we have.  

    **database table**: locations

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT country_id,  COUNT(*) 
        FROM locations   
        GROUP BY country_id; 

    |country_id	|count|
    |---|---|
    |BR	|1|
    |CA	|2|
    |"	|1|
    |SG	|1|
    |US	|4|
    |JP	|2|
    |IT	|2|
    |Ox	|1|
    |AU	|1|
    |NL	|1|
    |IN	|1|
    |CN	|1|
    |UK	|2|
    |CH	|2|
    |DE	|1|
___
26. Write a query in SQL to display the manager ID and number of employees managed by the manager.  

    **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT manager_id, COUNT(*) 
        FROM employees 
            GROUP BY manager_id;

    manager_id | count
    ----|------
    205 |     1
    122 |     8
    120 |     8
    101 |     5
    103 |     4
    108 |     5
    145 |     6
    100 |    14
    201 |     1
    124 |     8
    114 |     5
    121 |     8
    123 |     8
    102 |     1
    146 |     6
    147 |     6
    148 |     6
    149 |     6
    0 |     1
___
27. Write a query in SQL to display the details of jobs in descending sequence on job title.  

    **database table**: jobs

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT * 
        FROM jobs 
            ORDER BY job_title DESC;

    job_id    |job_title                      |min_salary|max_salary|
    ----------|-------------------------------|----------|----------|
    ST_MAN    |Stock Manager                  |      5500|      8500|
    ST_CLERK  |Stock Clerk                    |      2000|      5000|
    SH_CLERK  |Shipping Clerk                 |      2500|      5500|
    SA_REP    |Sales Representative           |      6000|     12000|
    SA_MAN    |Sales Manager                  |     10000|     20000|
    PU_MAN    |Purchasing Manager             |      8000|     15000|
    PU_CLERK  |Purchasing Clerk               |      2500|      5500|
    PR_REP    |Public Relations Representative|      4500|     10500|
    AC_ACCOUNT|Public Accountant              |      4200|      9000|
    IT_PROG   |Programmer                     |      4000|     10000|
    AD_PRES   |President                      |     20000|     40000|
    MK_REP    |Marketing Representative       |      4000|      9000|
    MK_MAN    |Marketing Manager              |      9000|     15000|
    HR_REP    |Human Resources Representative |      4000|      9000|
    FI_MGR    |Finance Manager                |      8200|     16000|
    AD_VP     |Administration Vice President  |     15000|     30000|
    AD_ASST   |Administration Assistant       |      3000|      6000|
    AC_MGR    |Accounting Manager             |      8200|     16000|
    FI_ACCOUNT|Accountant                     |      4200|      9000|


___
28. Write a query in SQL to display the first and last name and date of joining of the employees who is either Sales Representative or Sales Man.  

    **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT first_name, last_name, hire_date
        FROM employees 
            WHERE job_id IN ('SA_REP', 'SA_MAN');

    first_name  | last_name  | hire_date
    ------------|------------|------------
    John        | Russell    | 2004-10-01
    Karen       | Partners   | 2005-01-05
    Alberto     | Errazuriz  | 2005-03-10
    Gerald      | Cambrault  | 2007-10-15
    Eleni       | Zlotkey    | 2008-01-29
    Peter       | Tucker     | 2005-01-30
    David       | Bernstein  | 2005-03-24
    Peter       | Hall       | 2005-08-20
    Christopher | Olsen      | 2006-03-30
    Nanette     | Cambrault  | 2006-12-09
    Oliver      | Tuvault    | 2007-11-23
    Janette     | King       | 2004-01-30
    Patrick     | Sully      | 2004-03-04
    Allan       | McEwen     | 2004-08-01
    Lindsey     | Smith      | 2005-03-10
    Louise      | Doran      | 2005-12-15
    Sarath      | Sewall     | 2006-11-03
    Clara       | Vishney    | 2005-11-11
    Danielle    | Greene     | 2007-03-19
    Mattea      | Marvins    | 2008-01-24
    David       | Lee        | 2008-02-23
    Sundar      | Ande       | 2008-03-24
    Amit        | Banda      | 2008-04-21
    Lisa        | Ozer       | 2005-03-11
    Harrison    | Bloom      | 2006-03-23
    Tayler      | Fox        | 2006-01-24
    William     | Smith      | 2007-02-23
    Elizabeth   | Bates      | 2007-03-24
    Sundita     | Kumar      | 2008-04-21
    Ellen       | Abel       | 2004-05-11
    Alyssa      | Hutton     | 2005-03-19
    Jonathon    | Taylor     | 2006-03-24
    Jack        | Livingston | 2006-04-23
    Kimberely   | Grant      | 2007-05-24
    Charles     | Johnson    | 2008-01-04

___
29. Write a query in SQL to display the average salary of employees for each department who gets a commission percentage.  

    **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT department_id, AVG(salary) 
        FROM employees 
            WHERE commission_pct IS NOT NULL 
                GROUP BY department_id;

    department_id |          avg
    ---------------|------------------------
     90 |     19333.333333333333
     20 |  9500.0000000000000000
    100 |  8600.0000000000000000
     40 |  6500.0000000000000000
    110 | 10150.0000000000000000
     80 |  8955.8823529411764706
     70 | 10000.0000000000000000
     50 |  3475.5555555555555556
     60 |  5760.0000000000000000
     30 |  4150.0000000000000000
     10 |  4400.0000000000000000
      0 |  7000.0000000000000000

___
30. Write a query in SQL to display those departments where any manager is managing 4 or more employees.  

    **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT DISTINCT department_id
        FROM employees
            GROUP BY department_id, manager_id 
                HAVING COUNT(employee_id) >= 4;  

    department_id|
    ---------------|
     80|
     50|
     60|
    100|
     30|

___
31. Write a query in SQL to display those departments where more than ten employees work who got a commission percentage.  

    **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT department_id 
        FROM employees 
            WHERE commission_pct IS NOT NULL
                GROUP BY department_id 
                    HAVING COUNT(commission_pct) > 10;


    department_id|
    ---------------|
    80|
    50|
___
32. Write a query in SQL to display the employee ID and the date on which he ended his previous job.  

    **database table**: job_history

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT employee_id , MAX(end_date)
        FROM job_history
        WHERE employee_id 
            IN (SELECT employee_id
                FROM job_history
                GROUP BY 1
                HAVING COUNT(employee_id) > 1)
            GROUP BY 1

    employee_id |    max
    ------------|-----------
    101 | 2005-03-15
    200 | 2006-12-31
    176 | 2007-12-31
___

33. Write a query in SQL to display the details of the employees who have no commission percentage and salary within the range 7000 to 12000 and works in that department which number is 50.  

    **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT * 
        FROM employees 
            WHERE commission_pct IS NULL 
                AND salary BETWEEN 7000 AND 12000 
                    AND department_id = 50;

    employee_id | first_name | last_name | email | phone_number | hire_date | job_id | salary | commission_pct | manager_id | department_id
    -------------|------------|-----------|-------|--------------|-----------|--------|--------|----------------|------------|-------------
    (0 rows)

___
34. Write a query in SQL to display the job ID for those jobs which average salary is above 8000.  

    **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT job_id, AVG(salary) 
        FROM employees 
            GROUP BY job_id 
                HAVING AVG(salary)>8000;

    job_id   |          avg
    ------------|------------------------
    AC_ACCOUNT |  8300.0000000000000000
    SA_MAN     |     12200.000000000000
    AD_PRES    |     24000.000000000000
    AC_MGR     | 12000.0000000000000000
    FI_MGR     | 12000.0000000000000000
    MK_MAN     | 13000.0000000000000000
    PR_REP     | 10000.0000000000000000
    AD_VP      |     17000.000000000000
    SA_REP     |  8350.0000000000000000
    PU_MAN     | 11000.0000000000000000

___
35. Write a query in SQL to display job Title, the difference between minimum and maximum salaries for those jobs which max salary within the range 12000 to 18000.  

    **database table**: jobs

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT job_title, max_salary-min_salary AS salary_differences 
        FROM jobs 
        WHERE max_salary 
        BETWEEN 12000 AND 18000;

    job_title       | salary_differences
    -----------------|--------------------
    Finance Manager      |               7800
    Accounting Manager   |               7800
    Sales Representative |               6000
    Purchasing Manager   |               7000
    Marketing Manager    |               6000

___
36. Write a query in SQL to display all those employees whose first name or last name starts with the letter D.  

    **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT first_name, last_name 
        FROM employees 
            WHERE  first_name  LIKE 'D%' 
                OR last_name LIKE 'D%';

    first_name | last_name
    -----------|-----------
    Lex        | De Haan
    David      | Austin
    Diana      | Lorentz
    Daniel     | Faviet
    Den        | Raphaely
    Curtis     | Davies
    David      | Bernstein
    Louise     | Doran
    Danielle   | Greene
    David      | Lee
    Julia      | Dellinger
    Jennifer   | Dilly
    Donald     | OConnell
    Douglas    | Grant

___
37. Write a query in SQL to display the details of jobs which minimum salary is greater than 9000.  

    **database table**: jobs

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT * 
        FROM jobs 
        WHERE min_salary > 9000;

    job_id  |           job_title           | min_salary | max_salary
    --------|-------------------------------|------------|------------
    AD_PRES | President                     |      20000 |      40000
    AD_VP   | Administration Vice President |      15000 |      30000
    SA_MAN  | Sales Manager                 |      10000 |      20000

___
38. Write a query in SQL to display those employees who joined after 7th September, 1987.  

    **database table**: employees

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**Answer**

        SELECT * 
        FROM employees  
        WHERE hire_date > '1987-09-07';

    employee_id | first_name  |last_name|email|phone_number|hire_date|job_id|salary|commission_pct | manager_id | department_id
    -------------|-------------|-------|---------|-------|-----|----|------|--------|----|-------
    100 | Steven      | King        | SKING    | 515.123.4567       | 2003-06-17 | AD_PRES    | 24000.00 |          0.00 |        0 |            90
    101 | Neena       | Kochhar     | NKOCHHAR | 515.123.4568       | 2005-09-21 | AD_VP      | 17000.00 |           0.00 |      100 |            90
    102 | Lex         | De Haan     | LDEHAAN  | 515.123.4569       | 2001-01-13 | AD_VP      | 17000.00 |           0.00 |      100 |            90
    103 | Alexander   | Hunold      | AHUNOLD  | 590.423.4567       | 2006-01-03 | IT_PROG    |  9000.00 |           0.00 |      102 |            60
    104 | Bruce       | Ernst       | BERNST   | 590.423.4568       | 2007-05-21 | IT_PROG    |  6000.00 |           0.00 |      103 |            60
    105 | David       | Austin      | DAUSTIN  | 590.423.4569       | 2005-06-25 | IT_PROG    |  4800.00 |           0.00 |      103 |            60
    106 | Valli       | Pataballa   | VPATABAL | 590.423.4560       | 2006-02-05 | IT_PROG    |  4800.00 |           0.00 |      103 |            60
    107 | Diana       | Lorentz     | DLORENTZ | 590.423.5567       | 2007-02-07 | IT_PROG    |  4200.00 |           0.00 |      103 |            60
    108 | Nancy       | Greenberg   | NGREENBE | 515.124.4569       | 2002-08-17 | FI_MGR     | 12000.00 |           0.00 |      101 |           100
    109 | Daniel      | Faviet      | DFAVIET  | 515.124.4169       | 2002-08-16 | FI_ACCOUNT |  9000.00 |           0.00 |      108 |           100
    110 | John        | Chen        | JCHEN    | 515.124.4269       | 2005-09-28 | FI_ACCOUNT |  8200.00 |           0.00 |      108 |           100
    111 | Ismael      | Sciarra     | ISCIARRA | 515.124.4369       | 2005-09-30 | FI_ACCOUNT |  7700.00 |           0.00 |      108 |           100
    112 | Jose Manuel | Urman       | JMURMAN  | 515.124.4469       | 2006-03-07 | FI_ACCOUNT |  7800.00 |           0.00 |      108 |           100
    113 | Luis        | Popp        | LPOPP    | 515.124.4567       | 2007-12-07 | FI_ACCOUNT |  6900.00 |           0.00 |      108 |           100
    114 | Den         | Raphaely    | DRAPHEAL | 515.127.4561       | 2002-12-07 | PU_MAN     | 11000.00 |           0.00 |      100 |            30
    115 | Alexander   | Khoo        | AKHOO    | 515.127.4562       | 2003-05-18 | PU_CLERK   |  3100.00 |           0.00 |      114 |            30
    116 | Shelli      | Baida       | SBAIDA   | 515.127.4563       | 2005-12-24 | PU_CLERK   |  2900.00 |           0.00 |      114 |            30
    117 | Sigal       | Tobias      | STOBIAS  | 515.127.4564       | 2005-07-24 | PU_CLERK   |  2800.00 |           0.00 |      114 |            30
    118 | Guy         | Himuro      | GHIMURO  | 515.127.4565       | 2006-11-15 | PU_CLERK   |  2600.00 |           0.00 |      114 |            30
    119 | Karen       | Colmenares  | KCOLMENA | 515.127.4566       | 2007-08-10 | PU_CLERK   |  2500.00 |           0.00 |      114 |            30
    120 | Matthew     | Weiss       | MWEISS   | 650.123.1234       | 2004-07-18 | ST_MAN     |  8000.00 |           0.00 |      100 |            50
    121 | Adam        | Fripp       | AFRIPP   | 650.123.2234       | 2005-04-10 | ST_MAN     |  8200.00 |           0.00 |      100 |            50
    122 | Payam       | Kaufling    | PKAUFLIN | 650.123.3234       | 2003-05-01 | ST_MAN     |  7900.00 |           0.00 |      100 |            50
    123 | Shanta      | Vollman     | SVOLLMAN | 650.123.4234       | 2005-10-10 | ST_MAN     |  6500.00 |           0.00 |      100 |            50
    124 | Kevin       | Mourgos     | KMOURGOS | 650.123.5234       | 2007-11-16 | ST_MAN     |  5800.00 |           0.00 |      100 |            50
    125 | Julia       | Nayer       | JNAYER   | 650.124.1214       | 2005-07-16 | ST_CLERK   |  3200.00 |           0.00 |      120 |            50
    126 | Irene       | Mikkilineni | IMIKKILI | 650.124.1224       | 2006-09-28 | ST_CLERK   |  2700.00 |           0.00 |      120 |            50
    127 | James       | Landry      | JLANDRY  | 650.124.1334       | 2007-01-14 | ST_CLERK   |  2400.00 |           0.00 |      120 |            50
    128 | Steven      | Markle      | SMARKLE  | 650.124.1434       | 2008-03-08 | ST_CLERK   |  2200.00 |           0.00 |      120 |            50
    129 | Laura       | Bissot      | LBISSOT  | 650.124.5234       | 2005-08-20 | ST_CLERK   |  3300.00 |           0.00 |      121 |            50
    130 | Mozhe       | Atkinson    | MATKINSO | 650.124.6234       | 2005-10-30 | ST_CLERK   |  2800.00 |           0.00 |      121 |            50
    131 | James       | Marlow      | JAMRLOW  | 650.124.7234       | 2005-02-16 | ST_CLERK   |  2500.00 |           0.00 |      121 |            50
    132 | TJ          | Olson       | TJOLSON  | 650.124.8234       | 2007-04-10 | ST_CLERK   |  2100.00 |           0.00 |      121 |            50
    133 | Jason       | Mallin      | JMALLIN  | 650.127.1934       | 2004-06-14 | ST_CLERK   |  3300.00 |           0.00 |      122 |            50
    134 | Michael     | Rogers      | MROGERS  | 650.127.1834       | 2006-08-26 | ST_CLERK   |  2900.00 |           0.00 |      122 |            50
    135 | Ki          | Gee         | KGEE     | 650.127.1734       | 2007-12-12 | ST_CLERK   |  2400.00 |           0.00 |      122 |            50
    136 | Hazel       | Philtanker  | HPHILTAN | 650.127.1634       | 2008-02-06 | ST_CLERK   |  2200.00 |           0.00 |      122 |            50
    137 | Renske      | Ladwig      | RLADWIG  | 650.121.1234       | 2003-07-14 | ST_CLERK   |  3600.00 |           0.00 |      123 |            50
    138 | Stephen     | Stiles      | SSTILES  | 650.121.2034       | 2005-10-26 | ST_CLERK   |  3200.00 |           0.00 |      123 |            50
    139 | John        | Seo         | JSEO     | 650.121.2019       | 2006-02-12 | ST_CLERK   |  2700.00 |           0.00 |      123 |            50
    140 | Joshua      | Patel       | JPATEL   | 650.121.1834       | 2006-04-06 | ST_CLERK   |  2500.00 |           0.00 |      123 |            50
    141 | Trenna      | Rajs        | TRAJS    | 650.121.8009       | 2003-10-17 | ST_CLERK   |  3500.00 |           0.00 |      124 |            50
    142 | Curtis      | Davies      | CDAVIES  | 650.121.2994       | 2005-01-29 | ST_CLERK   |  3100.00 |           0.00 |      124 |            50
    143 | Randall     | Matos       | RMATOS   | 650.121.2874       | 2006-03-15 | ST_CLERK   |  2600.00 |           0.00 |      124 |            50
    144 | Peter       | Vargas      | PVARGAS  | 650.121.2004       | 2006-07-09 | ST_CLERK   |  2500.00 |           0.00 |      124 |            50
    145 | John        | Russell     | JRUSSEL  | 011.44.1344.429268 | 2004-10-01 | SA_MAN     | 14000.00 |           0.40 |      100 |            80
    146 | Karen       | Partners    | KPARTNER | 011.44.1344.467268 | 2005-01-05 | SA_MAN     | 13500.00 |           0.30 |      100 |            80
    147 | Alberto     | Errazuriz   | AERRAZUR | 011.44.1344.429278 | 2005-03-10 | SA_MAN     | 12000.00 |           0.30 |      100 |            80
    148 | Gerald      | Cambrault   | GCAMBRAU | 011.44.1344.619268 | 2007-10-15 | SA_MAN     | 11000.00 |           0.30 |      100 |            80
    149 | Eleni       | Zlotkey     | EZLOTKEY | 011.44.1344.429018 | 2008-01-29 | SA_MAN     | 10500.00 |           0.20 |      100 |            80
    150 | Peter       | Tucker      | PTUCKER  | 011.44.1344.129268 | 2005-01-30 | SA_REP     | 10000.00 |           0.30 |      145 |            80
    151 | David       | Bernstein   | DBERNSTE | 011.44.1344.345268 | 2005-03-24 | SA_REP     |  9500.00 |           0.25 |      145 |            80
    152 | Peter       | Hall        | PHALL    | 011.44.1344.478968 | 2005-08-20 | SA_REP     |  9000.00 |           0.25 |      145 |            80
    153 | Christopher | Olsen       | COLSEN   | 011.44.1344.498718 | 2006-03-30 | SA_REP     |  8000.00 |           0.20 |      145 |            80
    154 | Nanette     | Cambrault   | NCAMBRAU | 011.44.1344.987668 | 2006-12-09 | SA_REP     |  7500.00 |           0.20 |      145 |            80
    155 | Oliver      | Tuvault     | OTUVAULT | 011.44.1344.486508 | 2007-11-23 | SA_REP     |  7000.00 |           0.15 |      145 |            80
    156 | Janette     | King        | JKING    | 011.44.1345.429268 | 2004-01-30 | SA_REP     | 10000.00 |           0.35 |      146 |            80
    157 | Patrick     | Sully       | PSULLY   | 011.44.1345.929268 | 2004-03-04 | SA_REP     |  9500.00 |           0.35 |      146 |            80
    158 | Allan       | McEwen      | AMCEWEN  | 011.44.1345.829268 | 2004-08-01 | SA_REP     |  9000.00 |           0.35 |      146 |            80
    159 | Lindsey     | Smith       | LSMITH   | 011.44.1345.729268 | 2005-03-10 | SA_REP     |  8000.00 |           0.30 |      146 |            80
    160 | Louise      | Doran       | LDORAN   | 011.44.1345.629268 | 2005-12-15 | SA_REP     |  7500.00 |           0.30 |      146 |            80
    161 | Sarath      | Sewall      | SSEWALL  | 011.44.1345.529268 | 2006-11-03 | SA_REP     |  7000.00 |           0.25 |      146 |            80
    162 | Clara       | Vishney     | CVISHNEY | 011.44.1346.129268 | 2005-11-11 | SA_REP     | 10500.00 |           0.25 |      147 |            80
    163 | Danielle    | Greene      | DGREENE  | 011.44.1346.229268 | 2007-03-19 | SA_REP     |  9500.00 |           0.15 |      147 |            80
    164 | Mattea      | Marvins     | MMARVINS | 011.44.1346.329268 | 2008-01-24 | SA_REP     |  7200.00 |           0.10 |      147 |            80
    165 | David       | Lee         | DLEE     | 011.44.1346.529268 | 2008-02-23 | SA_REP     |  6800.00 |           0.10 |      147 |            80
    166 | Sundar      | Ande        | SANDE    | 011.44.1346.629268 | 2008-03-24 | SA_REP     |  6400.00 |           0.10 |      147 |            80
    167 | Amit        | Banda       | ABANDA   | 011.44.1346.729268 | 2008-04-21 | SA_REP     |  6200.00 |           0.10 |      147 |            80
    168 | Lisa        | Ozer        | LOZER    | 011.44.1343.929268 | 2005-03-11 | SA_REP     | 11500.00 |           0.25 |      148 |            80
    169 | Harrison    | Bloom       | HBLOOM   | 011.44.1343.829268 | 2006-03-23 | SA_REP     | 10000.00 |           0.20 |      148 |            80
    170 | Tayler      | Fox         | TFOX     | 011.44.1343.729268 | 2006-01-24 | SA_REP     |  9600.00 |           0.20 |      148 |            80
    171 | William     | Smith       | WSMITH   | 011.44.1343.629268 | 2007-02-23 | SA_REP     |  7400.00 |           0.15 |      148 |            80
    172 | Elizabeth   | Bates       | EBATES   | 011.44.1343.529268 | 2007-03-24 | SA_REP     |  7300.00 |           0.15 |      148 |            80
    173 | Sundita     | Kumar       | SKUMAR   | 011.44.1343.329268 | 2008-04-21 | SA_REP     |  6100.00 |           0.10 |      148 |            80
    174 | Ellen       | Abel        | EABEL    | 011.44.1644.429267 | 2004-05-11 | SA_REP     | 11000.00 |           0.30 |      149 |            80
    175 | Alyssa      | Hutton      | AHUTTON  | 011.44.1644.429266 | 2005-03-19 | SA_REP     |  8800.00 |           0.25 |      149 |            80
    176 | Jonathon    | Taylor      | JTAYLOR  | 011.44.1644.429265 | 2006-03-24 | SA_REP     |  8600.00 |           0.20 |      149 |            80
    177 | Jack        | Livingston  | JLIVINGS | 011.44.1644.429264 | 2006-04-23 | SA_REP     |  8400.00 |           0.20 |      149 |            80
    178 | Kimberely   | Grant       | KGRANT   | 011.44.1644.429263 | 2007-05-24 | SA_REP     |  7000.00 |           0.15 |      149 |             0
    179 | Charles     | Johnson     | CJOHNSON | 011.44.1644.429262 | 2008-01-04 | SA_REP     |  6200.00 |           0.10 |      149 |            80
    180 | Winston     | Taylor      | WTAYLOR  | 650.507.9876       | 2006-01-24 | SH_CLERK   |  3200.00 |           0.00 |      120 |            50
    181 | Jean        | Fleaur      | JFLEAUR  | 650.507.9877       | 2006-02-23 | SH_CLERK   |  3100.00 |           0.00 |      120 |            50
    182 | Martha      | Sullivan    | MSULLIVA | 650.507.9878       | 2007-06-21 | SH_CLERK   |  2500.00 |           0.00 |      120 |            50
    183 | Girard      | Geoni       | GGEONI   | 650.507.9879       | 2008-02-03 | SH_CLERK   |  2800.00 |           0.00 |      120 |            50
    184 | Nandita     | Sarchand    | NSARCHAN | 650.509.1876       | 2004-01-27 | SH_CLERK   |  4200.00 |           0.00 |      121 |            50
    185 | Alexis      | Bull        | ABULL    | 650.509.2876       | 2005-02-20 | SH_CLERK   |  4100.00 |           0.00 |      121 |            50
    186 | Julia       | Dellinger   | JDELLING | 650.509.3876       | 2006-06-24 | SH_CLERK   |  3400.00 |           0.00 |      121 |            50
    187 | Anthony     | Cabrio      | ACABRIO  | 650.509.4876       | 2007-02-07 | SH_CLERK   |  3000.00 |           0.00 |      121 |            50
    188 | Kelly       | Chung       | KCHUNG   | 650.505.1876       | 2005-06-14 | SH_CLERK   |  3800.00 |           0.00 |      122 |            50
    189 | Jennifer    | Dilly       | JDILLY   | 650.505.2876       | 2005-08-13 | SH_CLERK   |  3600.00 |           0.00 |      122 |            50
    190 | Timothy     | Gates       | TGATES   | 650.505.3876       | 2006-07-11 | SH_CLERK   |  2900.00 |           0.00 |      122 |            50
    191 | Randall     | Perkins     | RPERKINS | 650.505.4876       | 2007-12-19 | SH_CLERK   |  2500.00 |           0.00 |      122 |            50
    192 | Sarah       | Bell        | SBELL    | 650.501.1876       | 2004-02-04 | SH_CLERK   |  4000.00 |           0.00 |      123 |            50
    193 | Britney     | Everett     | BEVERETT | 650.501.2876       | 2005-03-03 | SH_CLERK   |  3900.00 |           0.00 |      123 |            50
    194 | Samuel      | McCain      | SMCCAIN  | 650.501.3876       | 2006-07-01 | SH_CLERK   |  3200.00 |           0.00 |      123 |            50
    195 | Vance       | Jones       | VJONES   | 650.501.4876       | 2007-03-17 | SH_CLERK   |  2800.00 |           0.00 |      123 |            50
    196 | Alana       | Walsh       | AWALSH   | 650.507.9811       | 2006-04-24 | SH_CLERK   |  3100.00 |           0.00 |      124 |            50
    197 | Kevin       | Feeney      | KFEENEY  | 650.507.9822       | 2006-05-23 | SH_CLERK   |  3000.00 |           0.00 |      124 |            50
    198 | Donald      | OConnell    | DOCONNEL | 650.507.9833       | 2007-06-21 | SH_CLERK   |  2600.00 |           0.00 |      124 |            50
    199 | Douglas     | Grant       | DGRANT   | 650.507.9844       | 2008-01-13 | SH_CLERK   |  2600.00 |           0.00 |      124 |            50
    200 | Jennifer    | Whalen      | JWHALEN  | 515.123.4444       | 2003-09-17 | AD_ASST    |  4400.00 |           0.00 |      101 |            10
    201 | Michael     | Hartstein   | MHARTSTE | 515.123.5555       | 2004-02-17 | MK_MAN     | 13000.00 |           0.00 |      100 |            20
    202 | Pat         | Fay         | PFAY     | 603.123.6666       | 2005-08-17 | MK_REP     |  6000.00 |           0.00 |      201 |            20
    203 | Susan       | Mavris      | SMAVRIS  | 515.123.7777       | 2002-06-07 | HR_REP     |  6500.00 |           0.00 |      101 |            40
    204 | Hermann     | Baer        | HBAER    | 515.123.8888       | 2002-06-07 | PR_REP     | 10000.00 |           0.00 |      101 |            70
    205 | Shelley     | Higgins     | SHIGGINS | 515.123.8080       | 2002-06-07 | AC_MGR     | 12000.00 |           0.00 |      101 |           110
    206 | William     | Gietz       | WGIETZ   | 515.123.8181       | 2002-06-07 | AC_ACCOUNT |  8300.00 |           0.00 |      205 |           110

___