# React 19 useEffect Bug: Infinite Loop and Performance Issues

This repository demonstrates a common bug in React 19 related to the `useEffect` hook. The problem arises from an improperly configured dependency array, causing the effect to run after every render, leading to performance issues and, in some cases, infinite loops.

## Bug Description

The `useEffect` hook in the provided `bug.js` file lacks a dependency array.  This means that the effect runs after every render, even if the relevant state values haven't changed. In the example, `console.log` is called repeatedly, demonstrating unnecessary work.

## Solution

The `bugSolution.js` file provides a corrected version. The dependency array `[count]` ensures the effect only runs when the `count` value changes.

## How to Reproduce

1. Clone the repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the console output in the browser's developer tools.