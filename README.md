# PHP Unset() in Foreach Loop Bug

This repository demonstrates a common error in PHP involving the use of `unset()` within a `foreach` loop. Modifying an array while iterating over it using `foreach` can lead to unexpected behavior because the internal pointer of the loop might skip elements.

## Bug Description
The `unset()` function removes an element from an array. When used within a `foreach` loop, it can cause the loop to skip elements. This is because when an element is removed, the array's internal pointer may jump, resulting in some elements being skipped. This often leads to unexpected results and logic errors.

## How to Reproduce
Run the `bug.php` file to observe the unexpected output.

## Solution
Use alternative approaches such as `array_filter()` to remove elements safely, ensuring that the loop continues without unexpected pointer jumps.