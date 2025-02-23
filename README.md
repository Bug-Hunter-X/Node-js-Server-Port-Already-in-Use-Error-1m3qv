# Node.js Server Port Already in Use

This repository demonstrates a common error in Node.js: attempting to start a server on a port that's already in use.  The `server.js` file contains the problematic code, while `serverSolution.js` provides a solution.

## Error Scenario

If you run `server.js` and port 8080 is already occupied by another process (e.g., another Node.js server or a different application), the server will fail to start and you'll likely see an error message similar to 'EADDRINUSE'.

## Solution

The `serverSolution.js` file shows how to handle this gracefully. It uses the `server.on('error', ...)` event listener to catch the `EADDRINUSE` error and respond appropriately, for example, by trying a different port or exiting gracefully.