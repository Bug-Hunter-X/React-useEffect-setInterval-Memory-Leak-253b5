# React useEffect setInterval Memory Leak

This repository demonstrates a common error in React applications involving the use of `setInterval` within the `useEffect` hook, leading to a memory leak.  The provided `bug.js` file shows the incorrect implementation, and `bugSolution.js` provides the corrected version.

**Problem:** The original code lacks a cleanup function in `useEffect`, resulting in `setInterval` continuing to run even after the component is unmounted.  This creates a memory leak and may lead to performance issues.

**Solution:** The solution introduces a cleanup function to `useEffect` which uses `clearInterval` to stop the interval timer when the component unmounts. This effectively prevents the memory leak.

This example highlights the importance of proper cleanup in `useEffect` when using timers or other asynchronous operations.