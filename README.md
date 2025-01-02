# Infinite useEffect Loop in React

This repository demonstrates a common React bug involving an infinite loop within the `useEffect` hook. The `useEffect` hook, without a proper dependency array, triggers after every render, leading to unnecessary re-renders and potential performance problems. This example highlights the importance of correctly specifying the dependencies within the `useEffect` hook's second argument.

## Bug Description

The `MyComponent` component uses the `useEffect` hook to log the current count to the console. However, because the dependency array is omitted, the effect runs after every render.  This creates an infinite loop, constantly updating the console and potentially impacting performance.

## Solution

The solution involves correctly specifying the dependency array in the `useEffect` hook.  The dependency array should list all variables used inside the useEffect function which are not declared inside that function. In this case, the `count` variable needs to be included in the dependency array.