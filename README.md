# Unhandled Errors in Node.js HTTP Server

This repository demonstrates a common error in Node.js applications: unhandled exceptions within HTTP request handlers.  Improper error handling can lead to server crashes and data loss.

The `bug.js` file shows an example of an HTTP server that throws an unhandled exception. The `bugSolution.js` demonstrates how to use error handling to gracefully handle such exceptions.

## How to reproduce the bug

1. Clone this repository.
2. Navigate to the repository directory.
3. Run `node bug.js`.
4. Open your browser and navigate to `http://localhost:3000/error`.  You'll see the server crash.

## Solution

The `bugSolution.js` file provides a more robust solution.  It uses a `try...catch` block within the request handler and a `server.on('error', ...)` event listener for handling server-level errors. 