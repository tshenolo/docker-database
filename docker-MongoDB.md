# Guide to MongoDB

## Introduction:
MongoDB is a popular, open-source NoSQL database that offers flexibility and scalability for modern applications. Its document-oriented data model makes it easy to store and manage data in a JSON-like format. This guide aims to provide step-by-step instructions for getting started with MongoDB using Docker, including pulling the MongoDB Docker image, running a MongoDB container, connecting to it, creating a database, inserting data, and querying data.

## Table of Contents:
1. Pulling the MongoDB Docker image
2. Running MongoDB container
3. Connecting to MongoDB container
4. Creating a database
5. Inserting data into MongoDB database
6. Querying data from MongoDB database

## 1. Pulling the MongoDB Docker image:
Before you can start using MongoDB with Docker, you need to pull the MongoDB Docker image from the Docker Hub repository. You can do this by running the following command in your terminal or command prompt:
```bash
docker pull mongo
```
This command will download the latest MongoDB image available on Docker Hub to your local machine.

## 2. Running MongoDB container:
Once you have the MongoDB image downloaded, you can run a MongoDB container using the following command:
```bash
docker run --name my-mongodb -d mongo
```
This command will start a new MongoDB container named my-mongodb in detached mode (-d), which means it will run in the background.

## 3. Connecting to MongoDB container:
To connect to the MongoDB container, you can use the docker exec command to access the MongoDB shell. Run the following command:
```bash
docker exec -it my-mongodb mongo
```
This command will open the MongoDB shell, allowing you to interact with the MongoDB instance running inside the container.

## 4. Creating a database:
Once you're connected to the MongoDB shell, you can create a new database using the use command. For example, to create a database named mydatabase, you can run:
```bash
use mydatabase
```

## 5. Inserting data into MongoDB database:
To insert data into a MongoDB database, you can use the insertOne() or insertMany() methods. For example, to insert a single document into a collection named mycollection, you can run:
```bash
db.mycollection.insertOne({ key: "value" })
```

## 6. Querying data from MongoDB database:
To query data from a MongoDB database, you can use the find() method. For example, to retrieve all documents from the mycollection collection, you can run:
```bash
db.mycollection.find()
```

## Conclusion:
MongoDB is a powerful NoSQL database that can be easily set up and managed using Docker. By following the steps outlined in this guide, you can quickly get started with MongoDB, from pulling the Docker image to querying data from your database. Whether you're building a small-scale application or a large-scale system, MongoDB provides the flexibility and scalability you need to store and manage your data effectively.





