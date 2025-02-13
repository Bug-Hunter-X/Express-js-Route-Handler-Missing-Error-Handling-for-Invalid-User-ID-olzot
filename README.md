# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers:  lack of error handling for invalid input.  The example shows a route that retrieves a user by ID.  The code attempts to parse the ID as an integer, but it fails to handle the case where the ID is not a valid number, resulting in an unhandled exception.

The `bug.js` file contains the buggy code.  The `bugSolution.js` file shows the corrected code with proper error handling.

## Bug
The original code lacks error handling for cases where `req.params.id` is not a valid integer. This can cause the application to crash or behave unpredictably if a non-numeric ID is passed to the route.

## Solution
The solution adds a `try...catch` block to handle potential errors during the integer parsing. If an error occurs, the route will return an appropriate error response (e.g., a 400 Bad Request).