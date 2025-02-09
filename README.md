# Node.js Server Freeze
This repository demonstrates a common Node.js issue: a server freezing due to a long-running synchronous operation within the request handler. This blocks the event loop, leading to unresponsive behavior.
The `server.js` file shows the problematic code.  The `server-solution.js` file provides a corrected version using asynchronous techniques.
## Problem:
The original code contains a loop that takes considerable time to execute. Because it's synchronous, it blocks the event loop, preventing the server from responding to other requests until the loop completes. 
## Solution:
The solution utilizes asynchronous operations to avoid blocking the event loop.  This ensures the server remains responsive even under heavy load.
## How to Run:
1. Clone this repository.
2. Navigate to the repository's directory.
3. Run `node server.js` for the buggy version and observe the behavior (the server will be unresponsive).
4. Run `node server-solution.js` to see how asynchronous operations maintain server responsiveness.