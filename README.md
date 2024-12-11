# Incorrect NaN Comparison in TypeScript

This repository demonstrates a common error in TypeScript comparison functions: the incorrect handling of NaN (Not a Number) values.

## Problem

The provided `compare` function uses strict equality (`===`) to check if two numbers are equal. However, `NaN === NaN` evaluates to `false`. This leads to an unexpected result when the function is called with NaN values. The function wrongly returns 0, implying equality when in fact the values are incomparable. 

## Solution

The solution employs the `Number.isNaN` method to explicitly check for NaN values before attempting a comparison.  If either input is NaN, the function appropriately returns an indication of incomparability.