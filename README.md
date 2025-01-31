# PHP array_merge() Unexpected Key Overwrite

This repository demonstrates a subtle bug in PHP related to the `array_merge()` function.  When merging arrays with overlapping numeric keys, the later array's values overwrite those from the earlier array. This behavior might not be immediately obvious and can lead to unexpected results in your application.

## The Bug
The provided `bug.php` file shows an example of this issue. Two arrays are merged using `array_merge()`, and the result is printed.  Observe that the value associated with key `2` is overwritten, demonstrating the unexpected behavior.

## The Solution
The `bugSolution.php` file offers a solution using `+` operator for array merging, or demonstrating the usage of array_replace_recursive().  This alternative approach preserves existing values.

## How to Reproduce
1. Clone this repository.
2. Run `bug.php` using a PHP interpreter.
3. Compare the output with the expected behavior (preserving the value 'banana').
4. Run `bugSolution.php` to see how to avoid this issue using the '+' operator or array_replace_recursive().

This demonstrates a critical consideration when working with array merging in PHP.