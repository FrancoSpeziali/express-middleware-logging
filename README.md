# Using middleware to log requests to an API

This project will have you building your own middleware

## What you will be doing

This project will allow you to practise using:

> Creating middleware in Express.js

This project assumes you've already had experience with:

> Express.js middleware
> Node.js filesystem

To do this project, you must have completed:

**express-solar-system-api**

## Tasks

## Task 1 - Writing your middleware function

Use the snippet **middleware template**

Your middleware should intercept **all** requests from the client, and write some data to a file

Each new line in the file should include the:

- `request.ip` - the ip of the client
- `request.method` - the method or type of request
- `request.originalUrl` - the original request url

## Task 2 - Reading the log, securely

- Create a new endpoint, which allows the user to **GET** all the data from the log file

The endpoint should read the log file and **respond** with all the data from the file

## Task 3 - Securing the log

- Write some middleware which will only allow requests through which include the query parameter `secret`, and where the query parameter `secret` matches a value (of your choice)

- Use this middleware to "protect" the endpoint you wrote in **Task 2**