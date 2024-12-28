# Firebase Silent Data Write Failure

This repository demonstrates a common, yet difficult-to-debug issue in Firebase: silent failures when writing large datasets.  The Firebase SDK may not provide clear error messages when attempting to write excessively large objects or arrays. This can lead to data loss without any obvious indication of the problem.

The `largeWriteBug.js` file shows how to reproduce the issue. The `largeWriteSolution.js` file provides a solution using batch writes to handle large datasets efficiently and prevent these silent errors.

## Reproducing the Bug

1. Clone the repository.
2. Install the Firebase SDK: `npm install firebase`
3. Configure your Firebase project and replace the placeholder values in `largeWriteBug.js` with your project's configuration.
4. Run `node largeWriteBug.js`.
5. Observe that the large data write fails silently (or with an unhelpful error).