# React useEffect Cleanup: Missing Return in setInterval
This example demonstrates a common error in React's `useEffect` hook: forgetting to include a cleanup function when using `setInterval`.  This can result in memory leaks and unexpected behavior.

## Problem
The `setInterval` function continues to run even after the component unmounts, leading to unnecessary updates and potential memory leaks.

## Solution
The solution is to return a cleanup function from `useEffect`.  This function will be called when the component unmounts, allowing us to stop the interval.