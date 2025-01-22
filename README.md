# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug causes an infinite rendering loop, ultimately crashing the application.

## Bug Description

The `useEffect` hook, when used without a proper dependency array, rerenders the component infinitely. This occurs because the effect function runs after every render, triggering a re-render, creating a cyclical dependency. 

## Solution

The solution is to correctly specify the dependencies in the dependency array. By including `count` in the array, the effect only runs when the `count` variable changes.