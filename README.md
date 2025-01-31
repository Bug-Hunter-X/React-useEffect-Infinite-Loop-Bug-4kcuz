# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: omitting a dependency from the dependency array. This can lead to infinite loops and unexpected behavior.

## Bug Description

The `useEffect` hook in `bug.js` is missing the `count` variable in its dependency array.  This causes the effect to run on every render, creating a cycle where the component re-renders, triggering the effect again and again.

## Solution

The `bugSolution.js` file shows the corrected code with `count` added to the dependency array. This ensures the effect only runs when the `count` value changes. 

## How to reproduce

1. Clone the repository.
2. Navigate to the directory `bug.js` in a terminal.
3. Run `npm start`.
4. Observe the behavior in the console.

## Note

Always double-check that your dependencies are correctly declared in `useEffect` to prevent unexpected behavior and performance issues. 