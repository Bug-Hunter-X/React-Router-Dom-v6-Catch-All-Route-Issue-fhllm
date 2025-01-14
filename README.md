# React Router Dom v6 Catch All Route Issue

This repository demonstrates a problem with the catch-all route (`path="*"`) in React Router v6.  The issue is that the catch-all route is always triggered, even when other routes should match.

## Problem Description

The `App.js` file contains a simple React Router setup. Despite having routes for `/` and `/about`, the catch-all route (`/*`) always renders, resulting in the `NotFound` component being displayed.  This isn't expected behavior, and indicates a potential misconfiguration or conflict within the router.

## Solution

The solution is provided in `AppSolution.js`. The problem is resolved by ensuring the catch-all route is placed at the very end of the route definitions in the `Routes` component.  This ensures that only when no other route matches, the catch-all route will be rendered.