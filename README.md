# Node.js Server Unresponsiveness

This repository demonstrates a common Node.js issue: server unresponsiveness caused by a long-running operation blocking the event loop.  The `server.js` file contains the problematic code, while `serverSolution.js` provides a solution using asynchronous operations.

## Problem

The original code performs a 5-second CPU-intensive loop within the request handler.  This blocks the event loop, making the server unresponsive to new requests during that time.  This is a classic example of a synchronous operation that should be handled asynchronously.

## Solution

The solution uses asynchronous operations to avoid blocking the event loop.  This allows the server to remain responsive, even while handling long-running tasks.

## How to run

1. Clone the repository.
2. Run `node server.js` to see the problem.
3. Run `node serverSolution.js` to see the solution.