# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug causes an infinite rendering loop, resulting in performance issues and potential crashes.  The solution highlights the importance of specifying a dependency array in `useEffect`.

## Bug Description

The `useEffect` hook, when called without a dependency array (`[]`), runs after every render.  In this case, updating `count` triggers a re-render, which in turn triggers the `useEffect` again, leading to an infinite loop.  This is often manifested as high CPU usage and the browser becoming unresponsive.

## Solution

The solution involves providing a dependency array to the `useEffect` hook.  The dependency array determines when the effect runs. By including `count` in the array, the effect only runs when the value of `count` changes.