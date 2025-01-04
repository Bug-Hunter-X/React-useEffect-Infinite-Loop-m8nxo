# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug occurs when the dependency array is omitted or incorrectly specified, leading to an infinite render loop.

## Bug Description

The `useEffect` hook in the `MyComponent` function lacks a proper dependency array. This causes the effect to run on every render, triggering a continuous update cycle. The `console.log` statement will illustrate this behaviour. The browser console may eventually display error message or become unresponsive.

## Solution

The solution involves correctly specifying the dependency array in the `useEffect` hook. By including `count` in the array, the effect will only re-run when the `count` state variable changes.