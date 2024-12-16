# Uncommon JavaScript Bug: Handling Multiple Null Arguments

This repository demonstrates a subtle bug in JavaScript function argument handling. The `foo` function aims to add two numbers but needs to gracefully handle null values. The initial implementation only checks for null individually, missing the scenario where both inputs are null simultaneously.

## Bug Description

The `foo` function correctly handles cases where one of the arguments ('a' or 'b') is null. However, if both 'a' and 'b' are null, it will still attempt to perform the addition of null + null, resulting in unexpected behavior or errors in other programming contexts (e.g., null + null in strict mode throws an error).

## Solution

The provided solution explicitly checks for the case where both arguments are null to prevent this error.