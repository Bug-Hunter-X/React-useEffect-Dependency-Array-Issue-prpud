# React useEffect Dependency Array Issue

This repository demonstrates a common error in React's `useEffect` hook: forgetting to include state variables in the dependency array.

## The Bug

The `bug.js` file contains a component with a `useEffect` hook that logs the current count.  However, the `count` variable is missing from the dependency array. This leads to the effect running on every render, causing an infinite loop of console logs and potentially performance issues.

## The Solution

The `bugSolution.js` file shows the corrected version. By including `count` in the dependency array (`[count]`), the effect now only runs when the `count` value changes, resolving the infinite loop problem.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install the necessary dependencies.
3. Run `npm start` to start the development server.
4. Observe the console output in the browser. In `bug.js` you will see an infinite loop.  `bugSolution.js` demonstrates the correct behavior.