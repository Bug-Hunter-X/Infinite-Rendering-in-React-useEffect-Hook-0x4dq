# React useEffect Infinite Rendering Bug

This repository demonstrates a common error in React's `useEffect` hook that leads to infinite rendering.  The problem arises from a missing dependency in the `useEffect` hook's dependency array, causing the effect to run on every render, triggering a state update, and thus resulting in an infinite loop.

## Bug
The `bug.js` file contains the problematic code. The `useEffect` hook lacks the `count` variable in its dependency array causing infinite rerenders.

## Solution
The `bugSolution.js` file shows the corrected code.  Adding `count` to the dependency array ensures that the effect only runs when `count` changes.