# React Router DOM v6 Unexpected Route Matching

This repository demonstrates an unexpected route matching behavior in React Router DOM v6 when a route path is a substring of another route path.

## Bug Description

When defining routes using the `Route` component, if one path is a substring of another, the shorter path will always match, regardless of its position in the routes array. This can lead to unexpected routing behavior.

## Reproduction Steps

1. Clone this repository.
2. Install dependencies: `npm install`
3. Run the application: `npm start`
4. Navigate to `/about`. You'll notice that it renders the `Home` component instead of the `About` component.

## Expected Behavior

Navigating to `/about` should render the `About` component.

## Actual Behavior

Navigating to `/about` renders the `Home` component.

## Solution

The solution involves using path parameters or more specific routes to prevent unintended matches. This repo includes a fix branch with a corrected implementation.