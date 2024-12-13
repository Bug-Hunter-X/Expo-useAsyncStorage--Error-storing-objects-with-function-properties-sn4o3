# Expo useAsyncStorage Bug: Objects with Functions

This repository demonstrates a bug encountered when using Expo's `useAsyncStorage` hook to store JavaScript objects that contain functions as properties.  The bug manifests as an error during the storage process, usually stemming from the inability to serialize functions.

## Reproduction Steps
1. Clone the repository.
2. Run `npm install` or `yarn install`.
3. Start the Expo development server.
4. Observe the error message logged to the console when attempting to store the object.

## Solution
The solution involves modifying the object before storage to remove or replace the function properties, then reconstructing the object after retrieval. This ensures only serializable data is stored and retrieved.

See `bugSolution.js` for a working example that addresses the problem.
