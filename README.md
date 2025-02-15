# Unhandled Promise Rejection in React Native Fetch

This repository demonstrates a common error in React Native applications: unhandled promise rejections stemming from network requests.  The `bug.js` file showcases the problematic code, while `bugSolution.js` provides a corrected version.

## Problem

The original code uses `async/await` with `fetch` but lacks comprehensive error handling.  If the network request fails, the error is not properly caught, potentially causing the application to crash or exhibit unexpected behavior.  This is a frequent source of instability in React Native apps.

## Solution

The solution involves implementing a robust `try...catch` block within the `useEffect` hook to handle potential errors during the fetch.  A `finally` block ensures that the loading state is updated regardless of success or failure, providing better user feedback.

## How to Reproduce

1. Clone this repository.
2. Navigate to the directory in your terminal.
3. Run `npm install` to install dependencies.
4. Run `npx react-native run-android` (or iOS equivalent) to start the app.
5. Observe the behavior with the initial `bug.js` file.
6. Replace `bug.js` with `bugSolution.js` and observe the improved error handling.
