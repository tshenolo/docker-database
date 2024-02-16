# Guide to Redis

## Introduction

Redis is an open-source, in-memory data structure store that can be used as a database, cache, and message broker. It supports various data structures such as strings, hashes, lists, sets, sorted sets with range queries, bitmaps, hyperloglogs, geospatial indexes, and streams. In this guide, we will cover the basics of using Redis within a Docker container environment, including pulling the Redis Docker image, running a Redis container, connecting to it, and performing basic operations like storing and retrieving data.

## Table of Contents
1. Pulling the Redis Docker Image
2. Running a Redis Container
3. Connecting to the Redis Container
4. Storing and Retrieving Data from Redis

## 1. Pulling the Redis Docker Image

To use Redis in a Docker environment, you need to start by pulling the Redis Docker image from the Docker Hub repository. You can do this using the docker pull command:
```bash
docker pull redis
```
This command will download the latest version of the Redis image to your local machine.

## 2. Running a Redis Container

Once you have pulled the Redis image, you can run a Redis container using the docker run command:
```bash
docker run --name my-redis-container -d redis
```
This command will create a new Docker container named my-redis-container running the Redis image in detached mode (-d), meaning it will run in the background.

## 3. Connecting to the Redis Container

After running the Redis container, you may want to connect to it to interact with the Redis server. You can do this using the docker exec command to execute commands inside the container:
```bash
docker exec -it my-redis-container redis-cli
```
This command will open an interactive Redis command-line interface where you can execute Redis commands.

## 4. Storing and Retrieving Data from Redis

Once connected to the Redis container, you can start storing and retrieving data using Redis commands. Here are some basic examples:

To set a key-value pair:
```sql
set mykey "Hello, Redis!"
```

To retrieve the value associated with a key:
```sql
get mykey
```

To set an expiration time for a key:
```sql
expire mykey 3600
```

To retrieve information about the Redis server:
```sql
info
```

These are just a few examples of what you can do with Redis. Refer to the Redis documentation for a comprehensive list of commands and their usage.

## Conclusion

Redis is a powerful in-memory data store that can be easily used within a Docker container environment. By following the steps outlined in this guide, you can quickly get started with Redis and begin leveraging its capabilities for caching, data storage, and more in your applications.