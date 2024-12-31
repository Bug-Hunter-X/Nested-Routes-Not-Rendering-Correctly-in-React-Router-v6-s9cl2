# React Router v6 Nested Route Bug

This repository demonstrates a common issue with nested routes in React Router v6. The problem is that the catch-all route (`/*`) is overriding nested routes, preventing them from rendering correctly.

## Bug Description

The provided `App.js` contains nested routes.  However, only the catch-all route (`/`) is ever rendered.  Expected behavior is that the nested route should render properly, but instead the catch-all route always renders, even when a more specific path exists.

## Solution

The solution in `AppSolution.js` demonstrates how to fix this issue by using the `useLocation` hook to get current route path name, and conditionally render components based on that path name.