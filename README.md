# React Router Dom Silent 404 Bug

This repository demonstrates a common, yet subtle bug in `react-router-dom` where navigating to an undefined route results in a silent 404 error. There's no error message or indication to the user that the route is invalid. This makes debugging challenging.  The solution involves adding a catch-all route to handle such scenarios.

## Bug Description
The bug occurs when using `react-router-dom`'s `Routes` and `Route` components without a fallback route to handle undefined paths.  When navigating to a URL that does not match any defined routes, the application simply renders nothing, leaving the user confused.

## Solution
The solution involves adding a `Route` component with the path `*` to act as a catch-all route. This component will render whenever the URL doesn't match any of the other defined routes.