# React Router v6 Catch-all Route Bug

This repository demonstrates a common issue encountered when using catch-all routes (`/*`) in React Router v6.  The problem arises when the catch-all route unintentionally overrides more specific routes, leading to incorrect page rendering.

## Problem Description

The `/*` route in `App.js` is intended to handle 404 errors. However, it's currently intercepting all routes, preventing navigation to other pages like `/about`. 

## Solution

The solution, provided in `AppSolution.js`, involves reordering the routes within the `<Routes>` component.  By placing the more specific routes *before* the catch-all route, React Router will correctly match them first.