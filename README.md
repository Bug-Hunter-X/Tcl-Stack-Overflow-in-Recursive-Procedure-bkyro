# Tcl Stack Overflow Bug

This repository demonstrates a stack overflow error in a recursive Tcl procedure. The `badproc` procedure is designed to calculate the factorial of a number, but it lacks a proper base case for the recursion, causing it to call itself infinitely until it runs out of stack space.

## Bug Description
The bug lies in the `badproc` procedure.  It recursively calls itself without checking for a base case where the recursion should stop (x == 0).  This results in unbounded recursion, leading to a stack overflow error.

## Bug Solution
The solution involves adding a proper base case to the `badproc` procedure. This ensures that the recursion terminates when x reaches 0. 

## How to reproduce the bug
1.  Run the `bug.tcl` file using a Tcl interpreter.
2.  Call the `badproc` procedure with a moderately large number (e.g., 1000) as input. 
3. Observe the stack overflow error.