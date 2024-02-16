# Guide to Microsoft SQL Server

## Introduction:
Microsoft SQL Server is a powerful relational database management system widely used in enterprise environments for storing, managing, and analyzing data. Docker is a popular platform for developing, shipping, and running applications in containers. By combining SQL Server with Docker, you can quickly set up and deploy SQL Server instances in a consistent and efficient manner.

This guide will walk you through the process of pulling the Microsoft SQL Server Docker image, running a SQL Server container, connecting to it, creating a database, creating a table within that database, inserting data into the table, and querying data from the database.

## Table of Contents:

1. Pulling the Microsoft SQL Server Docker image
2. Running SQL Server container
3. Connecting to SQL Server container
4. Creating a database
5. Creating a database table
6. Inserting data into SQL Server database
7. Querying data from SQL Server database

## Pulling the Microsoft SQL Server Docker image:

To get started, you need to pull the Microsoft SQL Server Docker image from the Docker Hub repository. You can do this using the following command:
```bash
docker pull mcr.microsoft.com/mssql/server
```
This command will download the latest version of the SQL Server image from the official Microsoft repository.

## 2. Running SQL Server container:

Once the image is downloaded, you can run a SQL Server container using the following command:
```bash
docker run -e "ACCEPT_EULA=Y" -e "SA_PASSWORD=YourStrong!Passw0rd" -p 1433:1433 --name sql_server_container -d mcr.microsoft.com/mssql/server
```
This command will start a new SQL Server container with the necessary environment variables configured.

## 3. Connecting to SQL Server container:

After the container is up and running, you can connect to it using SQL Server Management Studio (SSMS) or any other database management tool. Use the following connection parameters:

Server: localhost
Username: SA
Password: YourStrong!Passw0rd

```bash
sqlcmd -S localhost -U SA -P YourStrong!Passw0rd
```

## 4. Creating a database:

Once connected to the SQL Server instance, you can create a new database using SQL commands or through the management tool. For example:
```bash
CREATE DATABASE MyDatabase;
```

## 5. Creating a database table:

With the database created, you can proceed to create tables within it. Here's an example of creating a simple table:
```bash
USE MyDatabase;
CREATE TABLE MyTable (
    ID INT PRIMARY KEY,
    Name VARCHAR(50),
    Age INT
);
```

## 6. Inserting data into SQL Server database:

After creating the table, you can insert data into it using SQL INSERT statements:
```bash
INSERT INTO MyTable (ID, Name, Age) VALUES (1, 'John Doe', 30);
INSERT INTO MyTable (ID, Name, Age) VALUES (2, 'Jane Smith', 25);
```

## 7. Querying data from SQL Server database:

Finally, you can retrieve data from the table using SQL SELECT statements:
```bash
SELECT * FROM MyTable;
```
This will return all records from the MyTable table.

## Conclusion:

In this guide, you've learned how to effectively use Microsoft SQL Server with Docker, from pulling the SQL Server image to running containers, creating databases, tables, inserting data, and querying data. Leveraging Docker for SQL Server deployment offers flexibility, scalability, and consistency in managing your database environments. With these steps, you can efficiently set up and work with SQL Server in your development and production environments.









































