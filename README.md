# Inconsistent Behavior Accessing Non-Existent HTML Attributes

This repository demonstrates an uncommon bug related to accessing non-existent attributes in HTML.  While attempting to get a non-existent attribute using `getAttribute` returns null gracefully, performing operations on properties derived from such attributes (e.g., `toUpperCase` on `innerText` when the attribute is expected but missing) can lead to unexpected errors in certain browsers.  This inconsistency highlights the importance of robust error handling when working with HTML attributes.

The `bug.html` file showcases the problematic behavior, while `bugSolution.html` illustrates a more resilient approach.

## Bug Description

The primary issue is the inconsistent response between directly accessing a non-existent attribute versus using its derived properties. This can cause unexpected errors, especially in older browser environments.