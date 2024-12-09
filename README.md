# Unexpected NaN Comparison in JavaScript

This repository demonstrates a common yet subtle bug in JavaScript related to comparing NaN (Not a Number) values.

## The Problem

JavaScript's loose comparison (==) and strict comparison (===) operators both return `false` when comparing NaN to itself. This is counterintuitive because NaN represents an invalid numerical value.

The `bug.js` file provides a simple function illustrating this behavior.  The function checks if two numbers are equal; however, it fails to correctly identify NaN as being equal to itself.

## The Solution

The solution in `bugSolution.js` uses the `Number.isNaN()` function to reliably check for NaN.  `Number.isNaN()` correctly determines if a value is NaN, avoiding the unexpected behavior of direct comparison.

## How to reproduce

1. Clone the repository.
2. Open `bug.js` and `bugSolution.js`.
3. Run both files in a JavaScript environment (e.g., Node.js, browser's console).
4. Observe the difference in outputs.