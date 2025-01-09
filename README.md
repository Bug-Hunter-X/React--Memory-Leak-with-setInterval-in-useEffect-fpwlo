# React: Memory Leak with setInterval in useEffect

This repository demonstrates a common error in React applications: using `setInterval` within a `useEffect` hook without proper cleanup. This leads to memory leaks and unexpected behavior.

## Problem

The `bug.js` file contains a component that uses `setInterval` to update a counter every second.  However, it fails to clear the interval when the component unmounts, resulting in a memory leak.  Each time the component is rendered or unmounted, the interval continues to run in the background. 

## Solution

The `bugSolution.js` file provides the correct implementation.  It uses the return value of `useEffect` to clear the interval when the component unmounts, preventing memory leaks.

## How to Reproduce

1. Clone this repository.
2. Navigate to the directory.
3. Run `npm install`
4. Run `npm start`