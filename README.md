# Chai Code DevOps Assignment

## Assignment Description

The provided repository contains a basic full-stack application with the following components:

1. A basic Express.js server with basic & courses endpoint
2. A React.js frontend application
3. Redis integration for API response caching
4. MongoDB integration for data storage

## Objective

Your task is to containerize the application for a "Development" environment using Docker. Ensure that all components work seamlessly together within their respective containers and work as per the provided screenshots below.

## Note

The application environment variables are stored in a `.env` file. You can find the `.env.example` file in the respective directory. Copy it to `.env` and fill in the required values.

## How to Run the Containers

To start all the containers and seed the database, run the following command in your project root:

```sh
docker compose up -d && docker compose --profile seed run --rm chai-code-seeder
```

This will start all services in detached mode and run the database seeder. After this, your application will be ready for development.

### Note for Connecting to MongoDB from Host Machine

If you want to connect to the MongoDB instance running inside the container from your host machine (e.g., using MongoDB Compass or mongosh), use the following connection string:

```
mongodb://<username>:<password>@localhost:27018/chaicode?authSource=admin

# Example
mongodb://dummyuser:secret@localhost:27018/chaicode?authSource=admin
```

## Screenshots

### Home Page

![Screenshot 1](./screenshots/One.png)

### Load Data from MongoDB

![Screenshot 2](./screenshots/Two.png)

### API Response Caching

![Screenshot 3](./screenshots/Three.png)
