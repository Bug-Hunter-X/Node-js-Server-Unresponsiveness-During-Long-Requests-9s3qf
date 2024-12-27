# Node.js Server Unresponsiveness During Long Requests

This repository demonstrates a common issue in Node.js applications where long-running requests can cause the server to become unresponsive.  The `server.js` file contains the buggy code, while `serverSolution.js` provides a solution using asynchronous operations and event loops.

## Problem

The original `server.js` uses a synchronous `while` loop to simulate a long task. This blocks the event loop, preventing other requests from being processed. This leads to unresponsiveness and potential crashes under heavy load.

## Solution

The solution in `serverSolution.js` uses asynchronous operations and callbacks (or promises/async/await) to avoid blocking the event loop.  This allows the server to handle multiple requests concurrently without becoming unresponsive.