# MongoDB $inc Operator Unexpected Behavior
This example demonstrates an uncommon error related to the MongoDB `$inc` operator. The issue arises when attempting to decrement a counter that starts at zero using the `$inc` operator with a negative value.  This can lead to unexpected behavior, and this example highlights a robust solution.

## Bug
The bug lies in the improper usage of `$inc` with negative values when the field is initially absent or set to 0.

## Solution
The solution involves using `$inc` in conjunction with `$setOnInsert` to handle the case where the counter does not yet exist and adding error handling for situations where the counter's value reaches zero.