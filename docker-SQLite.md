#Guide to Using SQLite

## Introduction:
SQLite is a lightweight, self-contained, serverless, and open-source relational database management system (RDBMS). It's known for its simplicity, reliability, and ease of integration, making it a popular choice for embedded systems, mobile apps, and small-scale web applications. This guide aims to provide step-by-step instructions for working with SQLite, including pulling the SQLite Docker image, running a SQLite container, connecting to the container, creating a database, creating tables, inserting data, and querying data.

## Table of Contents:

1. Pulling the SQLite Docker Image
2. Running SQLite Container
3. Connecting to SQLite Container
4. Creating a Database
5. Creating a SQLite Database Table
6. Inserting Data into SQLite Database Table
7. Querying Data from SQLite Database

## 1. Pulling the SQLite Docker Image:
To get started with SQLite using Docker, you'll first need to pull the SQLite Docker image from the Docker Hub repository. You can do this using the following command:
```bash
docker pull sqlite
```

## 2. Running SQLite Container:
Once the SQLite image is downloaded, you can run a SQLite container using the following command:
```bash
docker run -it --name sqlite-container sqlite
```

3. Connecting to SQLite Container:
After running the SQLite container, you can connect to it using the following command:
```bash
docker exec -it sqlite-container sqlite3
```

4. Creating a Database:
To create a new SQLite database, you can use the following SQLite command within the container:
```sql
sqlite> .open your_database_name.db
```

5. Creating a SQLite Database Table:
Once the database is created, you can create a table using SQL commands. For example:
```sql
sqlite> CREATE TABLE users (
    id INTEGER PRIMARY KEY,
    name TEXT NOT NULL,
    email TEXT NOT NULL UNIQUE
);
```

6. Inserting Data into SQLite Database Table:
To insert data into the created table, you can use SQL INSERT statements. For example:
```sql
sqlite> INSERT INTO users (name, email) VALUES ('John Doe', 'john@example.com');
```

7. Querying Data from SQLite Database:
You can query data from the SQLite database table using SQL SELECT statements. For example:
```sql
sqlite> SELECT * FROM users;
```

## Conclusion:
SQLite provides a simple yet powerful solution for managing relational databases, and using it with Docker further enhances its flexibility and ease of use. By following the steps outlined in this guide, you can effectively work with SQLite, from setting up a container to performing database operations such as creating tables, inserting data, and querying information.















