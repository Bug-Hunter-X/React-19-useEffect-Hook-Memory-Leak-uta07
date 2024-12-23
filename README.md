# React 19 useEffect Hook Memory Leak

This repository demonstrates a common error in React 19 applications involving the `useEffect` hook.  Specifically, it showcases a missing `return` statement within a cleanup function, leading to potential memory leaks.

## Bug Description

The `bug.js` file contains a `MyComponent` which uses `useEffect` to log a message when the component mounts. However, it omits the necessary return statement for cleanup.  This can result in event listeners, timers, or other resources failing to be released when the component unmounts, leading to memory leaks in applications.

## Solution

The `bugSolution.js` file provides the correct implementation.  The added `return` statement ensures that any cleanup tasks are executed when the component is unmounted.  This prevents resource leaks and ensures efficient memory management.

## How to reproduce

1. Clone this repository
2. Run `npm install`
3. Run `npm start`
4. Observe the console output to see the bug in action.  The improved version in bugSolution.js will correct this.