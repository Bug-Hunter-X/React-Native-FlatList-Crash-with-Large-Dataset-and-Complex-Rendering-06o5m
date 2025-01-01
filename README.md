# React Native FlatList Crash with Large Dataset and Complex Rendering

This repository demonstrates a bug in React Native's FlatList component related to performance and crashes when handling large datasets with computationally expensive item renderers.  The bug is characterized by inconsistent crashes and the lack of helpful error messages, making debugging difficult.

## Bug Description

When using FlatList with a large dataset (e.g., 1000+ items) and components that require significant rendering or calculations within each item, the app may crash or freeze intermittently.  This is particularly noticeable on devices with limited resources.

## Reproduction Steps

1. Clone the repository.
2. Run `npm install`.
3. Run the app on a device or emulator.
4. Scroll through the FlatList.  Crashes may occur after repeated scrolling or at random intervals.

## Solution

The solution involves optimizing the rendering process to minimize the computational load on each item. Techniques like virtualization, memoization, and using more efficient components can significantly improve performance and prevent crashes.

See `FlatListBugSolution.js` for an implementation of these optimizations.