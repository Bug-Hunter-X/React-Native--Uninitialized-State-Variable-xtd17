# React Native Uninitialized State Variable Bug

This repository demonstrates a common bug in React Native applications: attempting to access a state variable before it has been fully initialized.  This often occurs when performing asynchronous operations that update state.  The `bug.js` file contains the buggy code. The `bugSolution.js` file provides a solution.

## Bug Description
The component attempts to use the `count` state variable before the `useEffect` hook has had a chance to set its value. This leads to an error because `count` is initially `undefined`.

## Solution
The solution utilizes optional chaining and nullish coalescing to handle the case where `count` is `undefined`. This ensures that the app will not crash and provides a default value instead.