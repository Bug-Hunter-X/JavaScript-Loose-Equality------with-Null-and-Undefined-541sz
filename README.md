# JavaScript Loose Equality Bug

This repository demonstrates a common, yet subtle, bug in JavaScript related to loose equality (`==`) when comparing `null` and `undefined`.  Loose equality doesn't reliably distinguish between these values, leading to unexpected behavior.

## The Problem

The provided `foo` function intends to return 0 if `x` is `null`, and `x + 1` otherwise.  However, due to the use of loose equality (`==`), calling `foo(undefined)` produces `NaN`, while the expected behavior might be to return 0.

## The Solution

Strict equality (`===`) should be used to explicitly check for `null` and `undefined` separately, ensuring precise comparison and avoiding unexpected behavior.

## How to reproduce the bug
1. Clone this repo
2. Navigate to the root folder
3. Run `node bug.js`

## How to fix the bug
1. Clone this repo
2. Navigate to the root folder
3. Run `node bugSolution.js`