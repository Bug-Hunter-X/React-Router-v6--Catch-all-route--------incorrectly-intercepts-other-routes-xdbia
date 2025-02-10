# React Router v6 Catch-All Route Bug

This repository demonstrates a bug in React Router v6 where a catch-all route (`/*`) unexpectedly intercepts other routes, even when a matching route exists.  This is counterintuitive and can lead to unexpected 404 errors.

## Problem Description

The provided `App.js` demonstrates a typical route setup using `react-router-dom` v6.  Despite having a route for `/about`, the catch-all route `/*` is always triggered, rendering the `NotFound` component.  This occurs regardless of the order of routes defined.

## Solution

This is resolved by using path="*" instead of path="/*"

## How to reproduce

1. Clone this repo.
2. Run `npm install`.
3. Run `npm start`.
4. Observe that navigating to `/about` displays the `Not Found` component instead of `About`.

## How to fix

Checkout the `solution` branch for a fix.