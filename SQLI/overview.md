\# SQL Injection Overview

SQL injection occurs when an attacker can modify SQL queries going to the SQL database in order to break the application's logic.





\## Why ?

* no input validation 
* direct concatenation of user input
* unsafe query construction





\## Impact

An attacker can:

* bypass the authentication (login bypass)
* have access to sensitive data (username,password,email…)
* modify the data in the database





\## Types



* UNION-based -> extract data that will be displayed directly in the response
* Error-based -> use database errors to discover its structure and reveal the data stored in the database
* Blind SQLI :

&#x20;      - Boolean-based -> true/false responses

&#x20;      - Time-based -> delayed responses



&#x20;   

\## Example - Login Bypass (lab PortSwigger)



Original query:

SELECT \* FROM users WHERE username='admin' AND password='foo'



Injection (in the username line):

admin'--



Result:

Password check is ignored -> access granted

