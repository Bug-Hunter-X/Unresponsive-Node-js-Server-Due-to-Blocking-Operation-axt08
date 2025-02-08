# Unresponsive Node.js Server

This repository demonstrates a common issue in Node.js: an unresponsive server caused by a long-running synchronous operation that blocks the event loop.  The `server.js` file contains the buggy code. The solution is provided in `serverSolution.js`.

## Bug Description

The server performs a 5-second CPU-bound task within the request handler. During this time, the server cannot accept any new requests, leading to unresponsiveness.

## Solution

The solution involves refactoring the long-running task to use asynchronous operations or offloading it to a worker thread.  The `serverSolution.js` file demonstrates the solution using asynchronous timers.