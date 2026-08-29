# LeetCode 85 – Maximal Rectangle

## Problem

Given a binary matrix containing only `0` and `1`, find the largest rectangle containing only `1`s and return its area.

## Example

### Input

```text id="n7gq2x"
matrix = [
    ["1","0","1","0","0"],
    ["1","0","1","1","1"],
    ["1","1","1","1","1"],
    ["1","0","0","1","0"]
]
```

### Output

```text id="u1q5ef"
6
```

The largest rectangle of `1`s has an area of `6`.

## Approach

I convert each row into a **histogram** of heights.

For every row:

1. Update the height of each column.
2. If the cell is `1`, increase its height.
3. If the cell is `0`, reset its height to `0`.
4. Find the largest rectangle in the histogram using a monotonic stack.
5. Keep track of the maximum area.

This uses the same idea as **LeetCode 84 – Largest Rectangle in Histogram**.

## Complexity

* **Time Complexity:** `O(M × N)`
* **Space Complexity:** `O(N)`

## Language

**Python**

## LeetCode

**Problem:** 85. Maximal Rectangle
**Difficulty:** Hard
**Topic:** Array, Dynamic Programming, Stack, Matrix

## Author

T.Nandhini
