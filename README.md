# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React's `useEffect` hook: an infinite loop caused by a missing dependency in the dependency array.  The `bug.js` file contains the buggy code.  `bugSolution.js` provides the corrected version.

## Bug Description

The `useEffect` hook in `bug.js` attempts to log the current count to the console. However, because `count` is not included in the dependency array, the effect runs on every render, causing the component to re-render constantly and the count to increase infinitely. This leads to a performance issue and potentially crashes the browser.

## Solution

The solution, shown in `bugSolution.js`, involves adding `count` to the dependency array of the `useEffect` hook. This ensures the effect only runs when the value of `count` changes.