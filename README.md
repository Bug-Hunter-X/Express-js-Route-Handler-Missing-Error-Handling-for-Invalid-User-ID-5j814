# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid user IDs.

The `bug.js` file contains the buggy code.  The route handler does not properly handle cases where the `userId` parameter is not a number or where a user with the specified ID is not found.  This can lead to unexpected behavior or crashes.

The `bugSolution.js` file provides a corrected version with proper error handling to address these issues.  It includes checks to ensure the `userId` is a number and gracefully handles the case where the user is not found.

## How to reproduce the bug

1. Clone this repository.
2. Run `npm install express` to install the required dependency.
3. Run `node bug.js`.
4. Access the route `/users/<invalid_id>` (e.g., `/users/abc`).

The application will likely crash or behave unexpectedly without proper error handling.