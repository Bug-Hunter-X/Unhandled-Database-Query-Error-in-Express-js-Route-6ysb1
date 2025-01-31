# Unhandled Database Query Error in Express.js Route

This repository demonstrates a common error in Express.js applications: inadequate error handling for database queries within route handlers.

## Bug Description
The `/users/:id` route attempts to fetch user details from a database.  If the user is not found, a 404 response is correctly returned. However, the code lacks error handling for scenarios where the database query itself fails (e.g., connection issues, invalid queries). This can lead to unexpected behavior or application crashes.

## Bug Solution
The solution introduces `try...catch` blocks to handle potential errors during database operations.  If an error occurs, a suitable error response (e.g., 500 Internal Server Error) is returned to the client.

## How to Reproduce the Bug
1. Clone the repository.
2. Install dependencies: `npm install`
3. Run the application: `node bug.js`
4. Simulate a database error (e.g., by intentionally causing a connection failure).
5. Observe the application behavior.