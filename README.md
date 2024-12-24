# JavaScript Closure Gotcha: Incorrect Loop Variable Value in setTimeout

This repository demonstrates a common JavaScript closure issue related to using loop variables within `setTimeout` callbacks.

## The Bug

The `bug.js` file contains a function `myFunction` that uses a `for` loop and `setTimeout` to log values to the console.  You might expect the code to print numbers 0 through 9, with a one-second delay between each number. However, due to closure behavior, the code incorrectly prints 10 ten times.

## The Solution

The `bugSolution.js` file provides a corrected version of `myFunction`. This uses an Immediately Invoked Function Expression (IIFE) to create a new scope for the loop variable 'i' ensuring correct values are logged.  Alternatively, let statements within the loop would also work. 

## How to Reproduce

1. Clone this repository.
2. Open the `bug.js` and `bugSolution.js` files in your preferred JavaScript environment.
3. Run the `myFunction` function in both files and observe the differences in output.

This example highlights the importance of understanding closure behavior when working with asynchronous operations and loops in JavaScript.