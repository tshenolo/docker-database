
# Guide to PostgreSQL with Docker

## Introduction:
PostgreSQL is a powerful open-source relational database management system known for its reliability, robustness, and extensive features. In this guide, we'll walk through the process of setting up PostgreSQL using Docker, running containers, connecting to them, creating databases, inserting and selecting data.

## Table of Contents:

1. Pulling the PostgreSQL Docker image
2. Running PostgreSQL container
3. Connecting to PostgreSQL container
4. Creating a database
5. Connect to the newly created database:
6. Creating a table in PostgreSQL
7. Inserting data into PostgreSQL database
8. Selecting data from PostgreSQL database

## 1. Pulling the PostgreSQL Docker image:
To start using PostgreSQL with Docker, you first need to pull the PostgreSQL image from Docker Hub. You can do this using the docker pull command:
```bash
docker pull postgres
```

## 2. Running PostgreSQL container:
Once the image is pulled, you can create and start a PostgreSQL container using the following command:
```bash
docker run --name my-postgres -e POSTGRES_PASSWORD=mysecretpassword -d postgres
```
Replace my-postgres with your preferred container name and mysecretpassword with your desired password.

## 3. Connecting to PostgreSQL container:
To connect to the PostgreSQL container, you can use the docker exec command to access the PostgreSQL command-line interface:
```bash
docker exec -it my-postgres psql -U postgres
```
Here, replace my-postgres with your container name and -U postgres with the PostgreSQL username.

## 4. Creating a database:
Once connected to the PostgreSQL container, you can create a new database using SQL commands:
```sql
CREATE DATABASE my_database;
```
Replace my_database with your preferred database name.


## 5. Connect to the newly created database:
Once you've executed the CREATE DATABASE command, you need to connect to the newly created database using the \c meta-command. In your case, you'd use:
```sql
\c my_database;
```
This command switches your session to the my_database database, allowing you to execute SQL commands within it

## 6. Creating a table in PostgreSQL
Once you have connected to your PostgreSQL container and selected your database, you can create a table to organize your data. Here's how you can do it:
```sql
CREATE TABLE employees (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100),
    age INTEGER,
    salary DECIMAL(10, 2)
);
```


## 7. Inserting data into PostgreSQL database:
After creating your table in PostgreSQL, you can start inserting data into it using the INSERT INTO statement. Here's how you can do it:
```sql
INSERT INTO employees (name, age, salary)
VALUES ('Jane Smith', 35, 60000.00),
       ('Michael Johnson', 40, 70000.00),
       ('Emily Brown', 28, 55000.00);
```

## 8. Selecting data from PostgreSQL database:
After inserting data into your PostgreSQL database, you can retrieve it using the SELECT statement. Here's how you can do it:
```sql
SELECT * FROM employees;
```

## Conclusion:
PostgreSQL is a versatile and powerful database management system, and with Docker, it becomes even easier to set up and manage. By following the steps outlined in this guide, you can quickly get started with PostgreSQL, create databases, insert and select data, and effectively manage your data storage needs.











