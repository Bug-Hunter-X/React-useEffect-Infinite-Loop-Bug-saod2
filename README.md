# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React applications: an infinite loop caused by incorrect usage of the `useEffect` hook.  The `useEffect` hook, while powerful, can easily lead to infinite loops if not used carefully.  This example shows the bug and its solution.

## Bug Description

The bug is caused by a missing dependency in the dependency array of the `useEffect` hook. The `useEffect` hook re-renders the component, leading to an infinite loop. 

## How to reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the console and see the infinite loop caused by the bug.

## Solution

The solution is to include `count` as a dependency in the `useEffect` hook's array. This ensures that the effect only runs when `count` changes, breaking the infinite loop.