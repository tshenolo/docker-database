# Guide to MySQL with Docker

## Introduction:
MySQL is a popular open-source relational database management system (RDBMS) that is widely used for managing structured data. Docker is a platform that allows you to package, distribute, and run applications in containers. In this guide, we will walk you through the process of setting up MySQL using Docker, from pulling the MySQL Docker image to performing basic operations like creating databases, inserting data, and querying data.

## Table of Contents:

1. Pulling the MySQL Docker image
2. Running MySQL container
3. Connecting to MySQL container
4. Creating a database
5. Inserting data into MySQL database
6. Selecting data from MySQL database

## 1. Pulling the MySQL Docker image:
Before you can start using MySQL with Docker, you need to pull the MySQL Docker image from the Docker Hub repository. You can do this by running the following command in your terminal or command prompt:
```bash
docker pull mysql
```

## 2. Running MySQL container:
Once you have pulled the MySQL Docker image, you can run a MySQL container by using the docker run command. Make sure to specify the necessary options such as the container name, port mappings, and environment variables for setting the MySQL root password. Here's an example command:
```bash
docker run --name mysql-container -e MYSQL_ROOT_PASSWORD=my-secret-pw -p 3306:3306 -d mysql
```

## 3. Connecting to MySQL container:
After running the MySQL container, you can connect to it using a MySQL client tool or command-line interface. For example, you can use the mysql command-line client to connect to the MySQL server running inside the container. Replace my-secret-pw with your actual root password set in the previous step.
```bash
mysql -h localhost -P 3306 -u root -p
```
Or
```bash
mysql -h 0.0.0.0 -P 3306 -u root -p
```
Or
```bash
docker exec -it mysql-container mysql -u root -p
```


## 4. Creating a database:
Once you are connected to the MySQL server, you can create a new database using SQL commands. For example, to create a database named my_database, you can execute the following SQL statement:
```bash
CREATE DATABASE my_database;
```

## 5. Creating a table:
Once you have created a database, you can create a table within that database to organize your data. Tables in MySQL consist of rows and columns, where each column has a specific data type. Here's how you can create a table named my_table with two columns (column1 and column2) in the my_database database:
```bash
USE my_database;

CREATE TABLE my_table (
    id INT NOT NULL AUTO_INCREMENT,
    column1 VARCHAR(255) NOT NULL,
    column2 VARCHAR(255) NOT NULL,
    PRIMARY KEY (id)
);
```

## 6. Inserting data into MySQL database:
After creating a table, you can insert data into it using SQL INSERT statements. Here's an example of inserting data into a table named my_table:
```bash
INSERT INTO my_table (column1, column2) VALUES ('value1', 'value2');
```

## 7. Selecting data from MySQL database:
To retrieve data from a MySQL database, you can use the SQL SELECT statement. For example, to select all records from the my_table table, you can execute the following SQL query:
```bash
SELECT * FROM my_table;
```

## Conclusion:
In this guide, we have covered the basic steps to set up MySQL using Docker, including pulling the MySQL Docker image, running a MySQL container, connecting to the container, creating databases, inserting data, and querying data. This should give you a good starting point for working with MySQL in a Docker environment.
























