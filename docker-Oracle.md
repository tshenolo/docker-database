# Guide to Using Oracle Docker Image 

## Introduction:
In this guide, we will walk through the process of utilizing the Oracle Docker image for managing a database. Docker allows for easy deployment and management of containers, providing a convenient environment for running applications and services. The Oracle Docker image we'll be using contains an Oracle Express Edition database, which is ideal for development, testing, and small-scale production use. By following the steps outlined in this guide, you'll be able to set up and interact with an Oracle database within a Docker container seamlessly.

## Table of Contents:
1. Pulling the Docker Image
2. Running the Docker Container
3. Connecting to the Database
4. Creating a New Schema
5. Connecting to the New Schema
6. Creating a Table
7. Inserting Data into the Table
8. Querying Data from Oracle Database Table

## 1. Pulling the Docker Image:
To pull the Oracle Docker image, execute the following command:
```bash
docker pull container-registry.oracle.com/database/express:latest
```

## 2. Running Oracle Container:
Once the image is pulled, you can run the Oracle container using the following command:
```bash
docker run --name oracle-container -d -p 1521:1521 -e ORACLE_SID=xe -e ORACLE_PDB=xe -e ORACLE_PWD=welcome123 container-registry.oracle.com/database/express:latest
```

## 3. Connecting to Oracle Container:
Connect to the running Oracle container using SQL*Plus or SQLcl with the provided credentials:

Use your preferred database client to connect to the Oracle database:

- Host: localhost
- Port: 1521
- Username: sys
- Password: welcome123
- SID: xe

```bash
docker exec -it oracle-container sqlplus sys/welcome123@//localhost:1521/XE as sysdba
```

## 4. Creating a New Schema:
After connecting to the database using the provided credentials execute the following SQL commands to create a new schema:
```sql
CREATE USER your_schema_name IDENTIFIED BY your_password;
```
```sql
GRANT CONNECT, RESOURCE TO your_schema_name;
```
```sql
GRANT UNLIMITED TABLESPACE TO your_schema_name;
```

NOTE: In Oracle Database 12c and later, common users and roles must have a prefix to differentiate them from local users and roles. Typically, common users and roles have a prefix of "C##" (e.g., C##docker)

## Connecting to the New Schema:
Disconnect from the system user and reconnect using the newly created schema:
```sql
DISCONNECT
```
```sql
CONNECT your_schema_name/your_password@localhost:1521/xe
```

## 6. Creating a Table:
Execute SQL commands to create a new table in the schema:
```sql
CREATE TABLE my_table (
    id NUMBER,
    name VARCHAR2(50)
);
```

## 7. Inserting Data into the Table:
Insert data into the newly created table:
```sql
INSERT INTO my_table (id, name) VALUES (1, 'John');
```

## 8. Querying Data from Oracle Database Table:
Retrieve data from the table using SQL commands. For instance:
```sql
SELECT * FROM my_table;
```

## Conclusion
This guide has provided a step-by-step walkthrough for pulling the Oracle Docker image, running a container, connecting to it, creating a database, managing tables, and performing basic data operations. With this knowledge, you can effectively utilize Oracle databases within Docker containers for your development and testing needs.
