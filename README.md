# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug causes an infinite loop due to a missing dependency in the `useEffect` dependency array.

## Bug Description
The `MyComponent` component uses `useEffect` to log the render count. However, it's missing `count` from its dependency array. This means that the effect runs on every render, causing the component to re-render constantly and leading to an infinite loop.

## Solution
The solution involves adding the `count` variable to the dependency array of the `useEffect` hook. This ensures the effect only runs when the `count` value changes.