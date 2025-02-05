# Express.js Route Handler Missing Return Statement

This repository demonstrates a common error in Express.js route handlers: missing a `return` statement within a conditional block.  This can lead to unexpected behavior and logical errors. 

## Bug
The `bug.js` file contains a route handler that fetches user data. If the user is not found, it sends a 404 status. However, due to the missing return statement, both the 404 response and the `res.send(userData)` are executed, resulting in unexpected behavior. 

## Solution
The `bugSolution.js` file provides the corrected route handler with the `return` statement added to the if condition, ensuring that only one response is sent.

## How to run:
1. Clone the repository.
2. Navigate to the repository directory.
3. Run `npm install express`.
4. Run `node bug.js` and `node bugSolution.js` to see the difference in behavior.