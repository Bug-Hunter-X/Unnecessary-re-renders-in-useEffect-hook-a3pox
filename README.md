# Unnecessary Re-renders in useEffect Hook

This repository demonstrates a common React bug involving the `useEffect` hook causing unnecessary re-renders.  The `useEffect` hook, without proper dependency array handling, runs after every render, leading to performance issues and potential unexpected behavior.

## Bug Description

The provided `MyComponent` uses `useEffect` to log the current count to the console. Because the dependency array is missing, the effect runs after every render, resulting in excessive logging. This is inefficient and, in more complex components, could lead to significant performance problems.

## Solution

The solution involves correctly specifying the dependency array for `useEffect`. By including `count` in the dependency array, the effect only runs when `count` changes, significantly improving performance.

## How to reproduce

Clone this repository and run `npm install`. Then, run `npm start` to start the development server. Observe the console logs - you'll see 'Count:' logged on every click, demonstrating the unnecessary re-renders.

## How to fix

Refer to the `bugSolution.js` file to see how to fix this by adding the dependency array to the useEffect hook.