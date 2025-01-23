# React useEffect setInterval Memory Leak
This repository demonstrates a common mistake when using the `useEffect` hook with `setInterval` in React, leading to a memory leak.  The component continuously updates the counter, never clearing the interval, even after unmounting.

## Bug Description
The `setInterval` function within the `useEffect` hook is not properly cleaned up, resulting in a memory leak.  The interval continues to run even after the component is unmounted.

## Solution
The solution involves using the cleanup function provided by `useEffect` to `clearInterval` before the component is unmounted. This ensures that the interval is properly stopped, preventing the memory leak.
