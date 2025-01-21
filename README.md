# React useEffect Hook Missing Dependency

This repository demonstrates a common error in React's `useEffect` hook: omitting a necessary dependency from the dependency array. This can lead to unexpected behavior and difficult-to-debug issues.

## The Bug

The `bug.js` file contains a component that uses the `useEffect` hook to log the current value of a counter variable.  However, the `count` variable is missing from the dependency array. This means that the effect will only run once after the initial render, even though the `count` variable changes on each click. This is because it is not checking for updates to count.

## The Solution

The `bugSolution.js` file shows the corrected code. By including `count` in the dependency array (`[count]`), the effect now correctly runs whenever the `count` variable changes, providing the expected behavior.