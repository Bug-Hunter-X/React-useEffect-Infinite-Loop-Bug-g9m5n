# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook. The bug arises from an incorrectly specified dependency array, leading to an infinite render loop.

## Bug Description

The `useEffect` hook is designed to perform side effects after every render.  However, if the dependency array is missing or incorrectly defined, the effect will run continuously, causing an infinite loop.

## Bug Reproduction

1. Clone the repository.
2. Navigate to the directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.
5. Observe the console output and the browser behavior. You'll see that the console logs infinitely, and the application likely becomes unresponsive.

## Solution

The solution involves correctly defining the dependency array for the `useEffect` hook.  Ensure that any values used within the effect are listed in the dependency array. If no values from the component's state are used in the effect, use an empty array `[]` as a dependency, which will ensure that the effect only runs after the initial render.