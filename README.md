# Using middleware to log requests to an API

This project will have you building your own middleware, to log requests to an API

## What you will be doing

This project will allow you to practise using:

> Creating middleware in Express.js

This project assumes you've already had experience with:

> Express.js middleware
> Node file system

To do this project, you must have completed:

**express-solar-system-api**

## Tasks

### Task 1

1. Create a `middleware.js` file

2. Use the following code to bootstrap your logger middlware;

```javascript
function logger(request, response, next) {
  next();
}
```

### Task 2 - Writing your middleware function

Update the logger middleware so that it intercepts **all** requests from the client, and use `console.log()` to display the following information about the request;

- `request.ip` - the ip of the client
- `request.method` - the method or type of request
- `request.originalUrl` - the original request url

Each of these values should be separated with a pipe character `|`, surrounded by a whitespace character.

For example:

```text
127.0.0.1 | GET | /planets/find
```

### Task 3 - Setting up the middleware

1. Using `app.use()`, inject the logger middleware you created into your application routing

   > Note: It should be used before any of your routes, otherwise the logging will not work

2. Test your express application by sending a request. You should see something displayed in the terminal.

### Task 4 - Storing the log into memory

In your logger middleware, use the `fs.writeFile()` method to write the log data into the file `LOG.txt`

### Task 5 - Reviewing the log

- Create a new endpoint, which allows the user to **GET** all the data from the log file

The endpoint should read the log file `LOG.txt` and **respond** with all the data from the file

> Hint: You can use `fs.readFile()` to read from a file
