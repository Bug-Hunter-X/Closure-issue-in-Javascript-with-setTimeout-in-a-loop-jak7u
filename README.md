# Closure issue in Javascript with setTimeout
This repository demonstrates a common closure issue in Javascript when using setTimeout inside a loop. The issue arises because the loop counter variable 'i' is not captured for each iteration of the loop. Instead, the value of 'i' is only captured when the setTimeout function finally executes, leading to unexpected behavior.

## The Problem
The code in `bug.ts` shows a function `printNumbers2` that attempts to print numbers from 1 to n using `setTimeout`. The expectation is that the numbers 1 to 5 will be printed. However, due to the closure issue, the value of `i` is captured after the loop has completed, resulting in 6 being printed five times.

## The Solution
The `bugSolution.ts` file demonstrates a solution to this problem by using an immediately invoked function expression (IIFE) to create a new scope for each iteration of the loop, ensuring that the correct value of `i` is captured.

## Running the Code
1. Clone the repository
2. Navigate to the repository directory
3. Compile and run the code using a typescript compiler (e.g., `tsc bug.ts && node bug.js`) and (e.g., `tsc bugSolution.ts && node bugSolution.js`)