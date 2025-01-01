# React Router v6 Catch-All Route Issue

This repository demonstrates a common issue encountered when using catch-all routes (`/*`) in React Router v6. The catch-all route, intended to handle all unmatched routes and display a 404 page, unexpectedly redirects to the home page. 

## Problem
The provided code uses React Router v6.  The `/*` route, meant to act as a 404 page, is not working correctly.  Instead of displaying the `NotFound` component for invalid URLs, it defaults to the `/` route.  This is inconsistent with expected behavior.

## Solution
The issue is resolved by ensuring that the catch-all route (`/*`) is placed last within the `Routes` component. React Router processes routes in order. If the catch-all route is not last, it might never be reached, because other routes may match first.