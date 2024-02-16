# Guide to Apache Cassandra

## Introduction

Apache Cassandra is a highly scalable, distributed NoSQL database management system designed to handle large amounts of data across many commodity servers, providing high availability and fault tolerance. This guide aims to provide a step-by-step walkthrough of common tasks when working with Cassandra, including pulling the Docker image, running Cassandra in a container, connecting to the container, creating keyspaces and tables, inserting data, and querying data.

## Table of Contents

1. Pulling the Cassandra Docker image
2. Running Cassandra container
3. Connecting to Cassandra container
4. Creating a keyspace and table
5. Inserting data into Cassandra database
6. Querying data from Cassandra database

## 1. Pulling the Cassandra Docker image:

To begin working with Cassandra using Docker, you need to pull the Cassandra image from Docker Hub. Use the following command to pull the latest Cassandra image:

```bash
docker pull cassandra
```
## 2. Running Cassandra container:

Once the Cassandra image is downloaded, you can run a Cassandra container using the following command:

```bash
docker run --name my-cassandra-container -d cassandra
```
This command will start a new Cassandra container named my-cassandra-container.

## 3. Connecting to Cassandra container:

To connect to the Cassandra container, you can use the docker exec command:

```bash
docker exec -it my-cassandra-container cqlsh
```
This command opens a CQL shell session inside the Cassandra container, allowing you to interact with Cassandra using CQL (Cassandra Query Language).

## 4. Creating a keyspace and table:

After connecting to the Cassandra container, you can create a keyspace and table using CQL commands. For example:

```sql
CREATE KEYSPACE my_keyspace WITH replication = {'class': 'SimpleStrategy', 'replication_factor': 1};
USE my_keyspace;
CREATE TABLE my_table (id UUID PRIMARY KEY, name TEXT, age INT);
```
This creates a keyspace named my_keyspace and a table named my_table within that keyspace.

## 5. Inserting data into Cassandra database:

You can insert data into the Cassandra table using CQL INSERT statements. For example:

```sql
INSERT INTO my_table (id, name, age) VALUES (uuid(), 'John', 30);
INSERT INTO my_table (id, name, age) VALUES (uuid(), 'Alice', 25);
```

## 6. Querying data from Cassandra database:

You can query data from the Cassandra table using CQL SELECT statements. For example:

```sql
SELECT * FROM my_table;
```

This will return all rows from the my_table table.

## Conclusion

This guide provided a step-by-step overview of working with Apache Cassandra using Docker. From pulling the Cassandra Docker image to querying data from a Cassandra database, you've learned essential tasks to get started with Cassandra in a Dockerized environment. Experiment with these commands and adapt them to your specific use cases to leverage the power of Cassandra for handling large-scale data.











