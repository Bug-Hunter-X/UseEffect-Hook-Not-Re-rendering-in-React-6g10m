# React useEffect Hook Not Re-rendering Bug

This repository demonstrates a common issue with the React `useEffect` hook where it does not re-render as expected when a state variable changes.  The problem is demonstrated in `bug.js`. The solution is provided in `bugSolution.js`.

## Problem

The `useEffect` hook is intended to perform side effects after a component renders. In this example, it logs a message to the console each time the component renders. However, the provided implementation incorrectly prevents re-rendering, leading to the console log not updating correctly when the state changes.

## Solution

The issue is resolved by correctly specifying the dependencies array in `useEffect`.  The `count` variable must be included in the dependencies array.  This ensures that the effect runs whenever `count` changes, resulting in the expected re-rendering and console log updates.
