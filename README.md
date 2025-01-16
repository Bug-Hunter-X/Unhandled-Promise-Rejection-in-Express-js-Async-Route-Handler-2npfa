# Unhandled Promise Rejection in Express.js Async Route Handler

This repository demonstrates a common error in Express.js applications: unhandled promise rejections in asynchronous route handlers.  The `bug.js` file showcases the problem. The `bugSolution.js` file provides a solution that uses `try...catch` to handle potential errors, improving the robustness of the application.

## Problem

Asynchronous operations, such as database queries or external API calls, are frequent in Express.js applications. If an error occurs during an asynchronous operation within a route handler and it's not properly handled, it results in an unhandled promise rejection. This can lead to crashes and make debugging difficult.

## Solution

The solution involves using `try...catch` blocks to gracefully handle potential errors, preventing unhandled rejections. This allows for better logging and more controlled error responses to clients.