# December-Of-Algorithms-Easy

## 1. Snack Pair Counter

### Problem Statement

A school is organizing a snack distribution event where students receive snack packs with assigned points. Given an integer array `points` and an integer `target`, count the number of non-adjacent pairs (`i < j` where `j - i > 1`) such that `points[i] + points[j] == target`.

### Input Format
- Line 1: An integer `n` (number of snack packs).
- Line 2: `n` space-separated integers representing `points`.
- Line 3: An integer `target`.

### Output Format
- Print a single integer representing the total number of valid non-adjacent pairs.

### Sample Input 1
5
1 2 4 5 3
6

### Sample Output 1
1

### Sample Input 2
5
3 1 2 4 2
5

### Sample Output 2
3

### Sample Input 3
4
1 2 3 4
10

### Sample Output 3
0

### Explanation
- **Sample 1:** Valid pair is `(1, 5)` at indices `(0, 3)` summing to `6`.
- **Sample 2:** Valid non-adjacent pairs summing to `5` are `(3, 2)` at `(0, 2)`, `(3, 2)` at `(0, 4)`, and `(1, 4)` at `(1, 3)`.
- **Sample 3:** No non-adjacent pairs sum to `10`.

### Constraints
- `2 ≤ n ≤ 1000`
- `-1000 ≤ points[i] ≤ 1000`
- `-2000 ≤ target ≤ 2000`

### Reference
### Reference

- [Codeforces 1538C – Number of Pairs](https://codeforces.com/problemset/problem/1538/C) — Counts pairs whose sum lies within a specified range.
- [Codeforces 2051D – Counting Pairs](https://codeforces.com/problemset/problem/2051/D) — Counts pairs satisfying a condition involving the array sum.


