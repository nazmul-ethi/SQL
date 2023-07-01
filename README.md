
### What is SQL?

Structured Query Language, or SQL, is the language that helps manage databases. It helps in creating data, operating on it, and retrieving it. It is also the standard language used in the Relational Database Systems. Various Relational Database Systems like MySQL, Sybase, Oracle, MS Access, Postgres, Infomix, SQL Server, MariaDB, and SQLite etc., have SQL as their base language.

### SQL VS NoSQL
| Comparison criteria | SQL | NoSQL |
|----------------------|---------------------|--------------------|
|Type of database | Relational | Non-relational|
|How is data stored? | Structured data in tables | Unstructured data in JSON files|
|Suitability for OLTP systems | Excellent | Average|
|Database compliance | ACID properties | CAP Theorem|

### SQL Process

When you run an SQL command against any RDBMS, the system figures out the best way to carry out your request, and the SQL engine figures out how to interpret it.

This procedure has a number of different components. Query Dispatcher, Optimization Engines, Classic Query Engine, and SQL Query Engine are some of these elements. Non-SQL queries are handled by the classic query engine, but logical files are not handled by the SQL query engine.


#### Here's what we need to learn to detect SQL injection.

     1. The SQL SELECT Statement
     2. SQL WHERE Clause
     3. SQL AND, OR and NOT Operators
     4. SQL ORDER BY Keyword
     5. SQL TOP, LIMIT, FETCH FIRST or ROWNUM Clause
     6. SQL COUNT(), AVG() and SUM() Functions
     7. The SQL LIKE Operator
     8. The SQL UNION Operator
     9. The SQL ANY and ALL Operators
    10. SQL CASE Expression
    11. SQL Comments
    12. SQL Arithmetic Operators - SQL Bitwise Operators -SQL Comparison Operators
    13. SQL Server SUBSTRING() Function
    14. SQL Server CONCAT() Function
    15. SQL Server ASCII() Function
    16. LEARN about database Schema
    
#### Some of The Most Important SQL Commands(Optional)

- **`SELECT`** - extracts data from a database
- **`UPDATE`** - updates data in a database
- **`DELETE`** - deletes data from a database
- **`INSERT INTO`** - inserts new data into a database
- **`CREATE DATABASE`** - creates a new database
- **`ALTER DATABASE`** - modifies a database
- **`CREATE TABLE`** - creates a new table
- **`ALTER TABLE`** - modifies a table
- **`DROP TABLE`** - deletes a table
- **`CREATE INDEX`** - creates an index (search key)
- **`DROP INDEX`** - deletes an index


### RDBMS
### What is RDBMS?
RDBMS stands for Relational Database Management System. It is an information management system that is oriented on a data model. Here all the information is properly stored as tables. RDBMS Example systems are SQL Server, Oracle, MySQL, MariaDB, and SQLite.

### Basic Features of RDBMS:
Offers information to be saved in the tables
Numerous users can access it together which is managed by a single user
Virtual tables are available for storing the insightful data
In order to exclusively find out the rows, the primary key is used
The data are always saved in rows and columns
To retrieve the information the indexes are used
Columns are being shared between tables using the keys

### RDBMS CONCEPTS
Relation in the RDBMS is the deposit of tuples having similar characteristics. A relation in RDBMS means the set of the entities and data contained in them. The entities are different instances and their relation is organized in different rows and columns in the data table.  The related information is of identical domains and constraints. By deleting old data and by inserting new data, relations are altered in the database model.

### Domain in RDBMS
The domain describes probable terms collected jointly that always have the same characteristics and also constraints. A domain can be involved in a feature but only if the feature is a factor of a particular set.

### RDBMS Database
The association between different databases is called the relational database. Here all the data are related in terms of the tables they are stored in. The users will be able to access them. RDBMS database is different from that of DBMS.

The RDBMS speaks about relations between different entities present in the database. Normal Database assists only the tables while RDBS along with the tables tells their connections too. Normal databases give consistent methods but databases of RDBMS do not offer any methodologies but instead give connections that connect one single object with another.

The stored database is called executable code. The database collects and saves data and that particular procedure is called the stored procedure. During this, the codes are also stored which are used for encapsulation, deleting, etc. The programmers are able to add extensions of the syntaxes of SQL due to the applications of the APIs in the stored processes.

### Database Schema
A database schema is a blueprint or definition of a database that describes the data types, columns, constraints, and relationships between tables. It is used to define the structure of a database and to ensure that data is stored in a consistent and organized way.

Yes, every database uses a schema. Some databases, such as Oracle, MySQL, PostgreSQL, and SQLite, have a built-in information schema that provides information about the database schema. The information schema is a database that contains metadata about the other databases in a database system. It can be used to query information about tables, columns, constraints, and other database objects.

The information schema does not store sensitive information, such as admin credentials. This information is typically stored in a separate table or file that is not accessible through the information schema.

Here are some of the benefits of using a database schema:

Data consistency: A database schema ensures that data is stored in a consistent and organized way. This makes it easier to query and analyze data, and it can help to prevent data corruption.
Data integrity: A database schema can be used to enforce data integrity constraints, such as unique keys and foreign keys. This helps to ensure that data is accurate and reliable.
Data security: A database schema can be used to control access to data. This can help to protect sensitive data from unauthorized access.
Here are some of the reasons why a database schema is important:

It provides a blueprint for the database. The schema defines the structure of the database, including the tables, columns, and relationships between them. This makes it easier to understand the database and to make changes to it.
It enforces data integrity. The schema can be used to define data constraints, such as unique keys and foreign keys. This helps to ensure that the data in the database is accurate and consistent.
It facilitates data access. The schema can be used to create views, which are virtual tables that provide a customized view of the data in the database. This makes it easier for users to access the data they need.
It simplifies data administration. The schema can be used to manage the database, such as creating and dropping tables, adding and removing columns, and changing data constraints. This makes it easier for database administrators to keep the database up to date.
Overall, a database schema is an essential part of any database. It provides a blueprint for the database, enforces data integrity, facilitates data access, and simplifies data administration.

###### References : [SQL Tutorial-W3schools](https://www.w3schools.com/sql/)


###### If you'd like to connect further, I invite you to follow my Twitter account.

[Twitter](https://twitter.com/nazmul_ethi)



#### Information gathering/reconnaissance tool list


| Tool name | Short description|
|------------------------------------|-----------------------------------------|
|1. [Amass](https://github.com/owasp-amass/amass)|Versatile subdomain enumerator using DNS, scraping, and logs. [BGP](https://bgp.he.net/)|
|2. [Subfinder](https://github.com/projectdiscovery/subfinder)|Fast passive subdomain discovery with search engines and DNS.[ONLINE TOOL](https://subdomainfinder.c99.nl/)|
|3. [Knock](https://github.com/guelfoweb/knock)|Subdomain scanner for generating potential subdomains.|
|4. [DNSrecon]()|dnsrecon is an automation tool used for DNS information gathering. It has many features but the one we'll mostly use is its brute force capabilities to try and find subdomains.|
|5. [Sublist3r](https://github.com/aboul3la/Sublist3r)|Python tool for finding subdomains with search engines and DNS.|
|6. [dig/nslookup](https://www.nslookup.io/domains/github.com/dns-records/)|These are separate DNS lookup tools, where "dig" is commonly used on Linux systems and "nslookup" is available on various operating systems|
|7. [Nmap](https://github.com/nmap/nmap)|A popular network scanning tool|
|8. [Masscan](https://github.com/robertdavidgraham/masscan)|A high-speed port scanner|
|9. [Httpx](https://github.com/projectdiscovery/httpx)|A tool for retrieving HTTP responses and gathering information|
|10. [eyewitness](https://github.com/RedSiege/EyeWitness)|A tool for capturing screenshots of web pages|
|11. [Waybackurls](https://github.com/tomnomnom/waybackurls)|A tool for extracting URLs from the Wayback Machine's archive|
|12. [Gospider/hakrawler](https://github.com/jaeles-project/gospider)|Both are web crawling tools used for website enumeration|
|13. [Ffuf](https://github.com/ffuf/ffuf)|A fast web fuzzer|
|14. [Dirsearch](https://github.com/maurosoria/dirsearch)|A tool for discovering directories and files on web servers|
|15. [Gobuster](https://github.com/OJ/gobuster)|A directory and file brute-forcing tool|
|16. [Kiterunner](https://github.com/assetnote/kiterunner)|kite is a context based webscanner that uses common api paths for content discovery of an applications api paths|
|17. [Whatweb](https://github.com/urbanadventurer/WhatWeb)|A tool for finding secrets, such as API keys, in source code|
|18. [Trufflenhog](https://github.com/trufflesecurity/trufflehog)|A tool for finding secrets, such as API keys, in source code|




| Term | Definition |
|----------------------|---------------------|
| ACK                | Acknowledgment is a message sent by the receiving end to confirm the successful receipt of data. |
| Congestion Control | A mechanism that manages the amount of data being sent over a network to prevent congestion. It helps to ensure that the network does not become overloaded and that data packets are delivered efficiently without causing significant delays or losses. |
| Error Detection | The process of identifying errors or corrupted data during transmission. It involves adding checksums or CRC (Cyclic Redundancy Check) values to the data, allowing the receiver to verify the integrity of the received data. If errors are detected, appropriate actions can be taken. |
| Flow Control | A technique used to manage the rate of data transmission between two devices. It ensures that the sender does not overwhelm the receiver with data faster than it can process or store. Flow control prevents data loss and buffer overflows by regulating the flow of data packets |
| MTU | Maximum Transmission Unit represents the maximum size of a packet that can be transmitted over a network. It defines the maximum amount of data that can be carried in one network packet.When data is larger than the MTU, it needs to be fragmented into smaller packets for transmission.  
| Port | A numerical identifier used to specify a particular process or service in a computer network. Ports allow multiple applications or services to coexist on the same device by assigning each application or service a unique port number. Examples include port 80 for HTTP and port 22 for SSH. |
| Quality of Service | QoS refers to the capability of a network to provide different priority levels to different types of data. QoS mechanisms prioritize certain types of traffic, ensuring that critical data, such as real-time voice or video, receives higher priority than less time-sensitive data. |
| Reliable Delivery  | A guarantee that data will be successfully delivered to the recipient without errors or losses. Reliable delivery is typically provided by protocols such as TCP (Transmission Control Protocol), which includes mechanisms for error detection, acknowledgment, retransmission, and sequencing. |
| Segmentation | The process of dividing a message into smaller units or segments for transmission over a network. Segmentation allows large data blocks to be split into smaller, manageable units that can be efficiently transmitted and reassembled at the receiving end. TCP segments data for transmission. |
| TCP | Transmission Control Protocol is a reliable, connection-oriented protocol that provides error checking, flow control, congestion control, and sequencing for data transmission. TCP establishes a connection between sender and receiver, ensuring reliable delivery of data.  It guarantees that data is received in the correct order without errors or losses.  |
| UDP  | User Datagram Protocol is a connectionless protocol that provides faster but less reliable transmission compared to TCP. UDP does not establish a connection or provide error recovery  mechanisms. It is often used for real-time communication, such as streaming media or online gaming.|






|                    | TCP                                               | UDP                                  |
| ------------------ | ------------------------------------------------- | ------------------------------------ |
| **Protocol**       | Reliable, connection-oriented transport protocol    | Unreliable, connectionless transport  |
| **Handshake**      | Three-way handshake:                              | No handshake                         |
|                    | 1. Client sends a SYN (Synchronize) packet        |                                      |
|                    | 2. Server responds with SYN-ACK                   |                                      |
|                    |    (Synchronize-Acknowledge) packet               |                                      |
|                    | 3. Client acknowledges with an ACK (Acknowledge)  |                                      |
|                    |    packet                                         |                                      |
| **Reliability**    | Provides reliable delivery of data packets        | Provides best-effort delivery of     |
|                    | through acknowledgment, retransmission, and       | data packets without guaranteeing    |
|                    | sequencing mechanisms                             | delivery or order                    |
| **Connection**     | Establishes a connection before data transfer      | No connection establishment         |
|                    |                                                   | required                             |
| **Flow Control**   | Utilizes flow control mechanisms to regulate      | No inherent flow control mechanism   |
|                    | the rate of data transmission to prevent          |                                      |
|                    | overwhelming the receiver                          |                                      |
| **Congestion       | Implements congestion control algorithms           | No built-in congestion control       |
| Control**          | to manage network congestion and ensure            | mechanisms                           |
|                    | fair and efficient data transmission               |                                      |
| **Usage**          | Suitable for applications requiring reliable       | Suitable for real-time applications, |
|                    | and ordered delivery of data (e.g., web            | multimedia streaming, online gaming  |
|                    | browsing, file transfer)                           |                                      |
| **Examples**       | HTTP, FTP, SMTP, SSH, Telnet                      | DNS, VoIP, streaming applications    |

