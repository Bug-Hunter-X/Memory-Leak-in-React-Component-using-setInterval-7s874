# React setInterval Memory Leak

This repository demonstrates a common error in React components: using `setInterval` within the `useEffect` hook without proper cleanup. This leads to a memory leak as the interval continues even after the component unmounts.

The `bug.js` file showcases the problematic code.  The solution, demonstrating the correct implementation, is in `bugSolution.js`.

## Bug
The bug is the missing cleanup function in the `useEffect` hook.  Without it, the interval continues to run even after the component is unmounted, leading to a memory leak.

## Solution
The solution uses the return value of `useEffect` to provide a cleanup function. This function clears the interval when the component unmounts, preventing the memory leak.
