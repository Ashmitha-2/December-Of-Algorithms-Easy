# December-Of-Algorithms-Easy

## 1. Snack Pair Counter

### Problem Statement

A school is organizing a snack distribution event where students receive snack packs with assigned points. Given an integer array points and an integer target, count the number of non-adjacent pairs (i < j where j - i > 1) such that points[i] + points[j] == target.

### Input Format

- Line 1: An integer n (number of snack packs).
- Line 2: n space-separated integers representing points.
- Line 3: An integer target.

### Output Format

Print a single integer representing the total number of valid non-adjacent pairs.

### Sample Input 1

```text
5
1 2 4 5 3
6
```

### Sample Output 1

```text
1
```

### Sample Input 2

```text
5
3 1 2 4 2
5
```

### Sample Output 2

```text
3
```

### Sample Input 3

```text
4
1 2 3 4
10
```

### Sample Output 3

```text
0
```

### Explanation

- Sample 1: Valid pair is (1, 5) at indices (0, 3) summing to 6.
- Sample 2: Valid non-adjacent pairs summing to 5 are (3, 2) at (0, 2), (3, 2) at (0, 4), and (1, 4) at (1, 3).
- Sample 3: No non-adjacent pairs sum to 10.

### Constraints

- 2 ≤ n ≤ 1000
- -1000 ≤ points[i] ≤ 1000
- -2000 ≤ target ≤ 2000

### Reference

- [Codeforces 1538C – Number of Pairs](https://codeforces.com/problemset/problem/1538/C) — Counts pairs whose sum lies within a specified range.
- [Codeforces 2051D – Counting Pairs](https://codeforces.com/problemset/problem/2051/D) — Counts pairs satisfying a condition involving the array sum.

## 2. K-th Element of Two Sorted Arrays

### Problem Statement

Given two sorted arrays `a[]` and `b[]` and an integer `k`, find the element that would be at the `k`-th position (1-based indexing) of the combined sorted array.

### Input Format

- The first line contains three integers `n`, `m`, and `k`, representing the sizes of `a[]` and `b[]` and the target position `k`.
- The second line contains `n` space-separated integers for `a[]`.
- The third line contains `m` space-separated integers for `b[]`.

### Output Format

Print a single integer representing the `k`-th element of the combined sorted array.

### Sample Input 1

```text
5 4 5
2 3 6 7 9
1 4 8 10
```

### Sample Output 1

```text
6
```

### Sample Input 2

```text
5 5 6
1 4 8 10 12
5 7 11 15 17
```

### Sample Output 2

```text
10
```

### Explanation

In sample 1, the combined sorted array is `[1, 2, 3, 4, 6, 7, 8, 9, 10]`, and the 5th element is `6`. In sample 2, the combined sorted array is `[1, 4, 5, 7, 8, 10, 11, 12, 15, 17]`, and the 6th element is `10`.

### Constraints

- `1 ≤ n, m ≤ 10^5`
- `1 ≤ k ≤ n + m`
- `0 ≤ a[i], b[i] ≤ 10^9`
- Both arrays are sorted in non-decreasing order.

### Reference

- [GeeksforGeeks – K-th Element of Merged Two Sorted Arrays](https://www.geeksforgeeks.org/dsa/k-th-element-two-sorted-arrays/)


  ## 3. Roman Numeral Converter with Digit Sum

### Problem Statement

Roman numerals are represented using seven symbols: `I`, `V`, `X`, `L`, `C`, `D`, and `M`.

Given a valid Roman numeral string `s`, convert it into its decimal integer representation. After converting it, calculate the sum of all the digits of the resulting integer. Return both the converted integer and its digit sum.

### Input Format

- A single string `s` representing a valid Roman numeral.

### Output Format

Print two integers separated by a space:
1. The decimal integer equivalent of the Roman numeral.
2. The sum of the digits of that integer.

### Sample Input 1

```text
III
```

### Sample Output 1

```text
3 3
```

### Sample Input 2

```text
LVIII
```

### Sample Output 2

```text
58 13
```

### Sample Input 3

```text
MCMXCIV
```

### Sample Output 3

```text
1994 23
```

### Explanation

In sample 1, `III` equals `3`, and its digit sum is `3`. In sample 2, `LVIII` equals `58`, and `5 + 8 = 13`. In sample 3, `MCMXCIV` equals `1994`, and `1 + 9 + 9 + 4 = 23`.

### Constraints

- `1 ≤ length of s ≤ 15`
- `s` contains only valid Roman numeral symbols (`I`, `V`, `X`, `L`, `C`, `D`, `M`).
- The resulting integer is between `1` and `3999`.

### Reference

- [LeetCode – Roman to Integer](https://leetcode.com/problems/roman-to-integer/)

  ## 4. Project TRI-FLOW – Detect the Three-Phase Traffic Pattern

### Problem Statement

A smart city traffic management system monitors vehicle speeds at consecutive checkpoints and identifies a special three-phase speed pattern called a **Trionic Array**:
1. **Acceleration Phase:** Vehicle speed strictly increases.
2. **Deceleration Phase:** Vehicle speed strictly decreases.
3. **Re-acceleration Phase:** Vehicle speed strictly increases again.

All three phases must be non-empty (each must contain at least one transition), and equal adjacent elements are not allowed. Determine whether the given speed array represents a valid Trionic Array.

### Input Format

- The first line contains an integer `n`, representing the number of checkpoints.
- The second line contains `n` space-separated integers representing vehicle speeds recorded at each checkpoint.

### Output Format

Print `true` if the given array is a Trionic Array; otherwise, print `false`.

### Sample Input 1

~~~
7
1 3 5 4 2 6 8
~~~

### Sample Output 1

~~~
true
~~~

### Sample Input 2

~~~
6
1 2 3 4 5 6
~~~

### Sample Output 2

~~~
false
~~~

### Sample Input 3

~~~
6
1 4 3 2 5 4
~~~

### Sample Output 3

~~~
false
~~~

### Explanation

In sample 1, the speeds strictly increase (`1 → 3 → 5`), strictly decrease (`5 → 4 → 2`), and strictly increase again (`2 → 6 → 8`). In sample 2, the array only increases without a decreasing phase. In sample 3, the final phase decreases instead of increasing.

### Constraints

- `4 ≤ n ≤ 10^5`
- `0 ≤ speed[i] ≤ 10^9`
- Equal adjacent elements are not allowed in valid transitions.

### Reference

- LeetCode – Trionic Array I: https://leetcode.com/problems/trionic-array-i/

  ## 5. Two Sum with Minimum Index Distance

### Problem Statement

A college is organizing a technical event. Each student has a score, and the organizers want to find two students whose combined scores equal a given target score `T`, with at least `D` positions between their indices in the registration list.

Given an array `A` of `N` integers representing student scores, a target sum `T`, and a minimum index distance `D`, find two indices `i` and `j` such that:
1. `i < j`
2. `A[i] + A[j] == T`
3. `j - i >= D`

If multiple valid pairs exist, choose the pair with the smallest second index `j`. If there are multiple choices for the same `j`, choose the smallest first index `i`. If no valid pair exists, print `-1 -1`.

### Input Format

- The first line contains three integers `N`, `T`, and `D`.
- The second line contains `N` space-separated integers representing the array `A`.

### Output Format

Print two space-separated integers `i` and `j`, or `-1 -1` if no valid pair exists.

### Sample Input 1

~~~
5 9 2
2 7 11 15 2
~~~

### Sample Output 1

~~~
1 4
~~~

### Sample Input 2

~~~
4 6 3
3 2 4 3
~~~

### Sample Output 2

~~~
0 3
~~~

### Sample Input 3

~~~
3 10 2
5 5 1
~~~

### Sample Output 3

~~~
-1 -1
~~~

### Explanation

In sample 1, `(0, 1)` sums to `9` but has distance `1 < 2`, so `(1, 4)` (`7 + 2 = 9`, distance `3`) is chosen. In sample 2, `(0, 3)` sums to `6` with distance `3`. In sample 3, no pair sums to `10` with distance at least `2`.

### Constraints

- `2 ≤ N ≤ 10^5`
- `1 ≤ D < N`
- `-10^9 ≤ A[i], T ≤ 10^9`

### Reference

- LeetCode – Two Sum: https://leetcode.com/problems/two-sum/

  ## 6. Merge Two Sorted Lists (Excluding Negative Nodes)

### Problem Statement

You are given the heads of two sorted linked lists `list1` and `list2`.

Merge the two lists into one sorted list by splicing together the nodes of the first two lists. **Any node with a negative value must be left out of the merged list.** Return the head of the merged linked list.

### Input Format

- The first line contains two integers `n` and `m`, the lengths of `list1` and `list2`.
- The second line contains `n` space-separated integers for `list1` (omit if `n = 0`).
- The third line contains `m` space-separated integers for `list2` (omit if `m = 0`).

### Output Format

Print the space-separated values of the merged non-negative linked list, or `[]` if the resulting list is empty.

### Sample Input 1

~~~
3 3
-3 1 4
0 2 5
~~~

### Sample Output 1

~~~
0 1 2 4 5
~~~

### Sample Input 2

~~~
2 1
-2 -1
-5
~~~

### Sample Output 2

~~~
[]
~~~

### Sample Input 3

~~~
0 1
0
~~~

### Sample Output 3

~~~
0
~~~

### Explanation

In sample 1, `-3` is excluded and the remaining nodes merge into `[0, 1, 2, 4, 5]`. In sample 2, all nodes are negative and excluded, leaving an empty list `[]`. In sample 3, `0` is non-negative and remains in the merged list.

### Constraints

- The number of nodes in both lists is in the range `[0, 200]`.
- `-1000 ≤ Node.val ≤ 1000`
- Both `list1` and `list2` are sorted in non-decreasing order.

### Reference

-LeetCode – Merge Two Sorted Lists: https://leetcode.com/problems/merge-two-sorted-lists/

## 7. Sort an Array of Strings According to String Lengths

### Problem Statement

Given an array `arr[]` of strings, sort the strings in ascending order based on their lengths. If two strings have the same length, their original relative order must be preserved in the final output (stable sort).

### Input Format

- The first line contains an integer `n`, the number of strings.
- The second line contains `n` space-separated strings.

### Output Format

Print the `n` sorted strings separated by spaces.

### Sample Input 1

~~~
4
GeeksforGeeks I from am
~~~

### Sample Output 1

~~~
I am from GeeksforGeeks
~~~

### Sample Input 2

~~~
4
You are beautiful looking
~~~

### Sample Output 2

~~~
You are looking beautiful
~~~

### Explanation

In sample 1, the lengths are `13, 1, 4, 2`, so sorting in ascending order gives `I am from GeeksforGeeks`. In sample 2, `You` and `are` both have length `3`, so `You` stays before `are`, followed by `looking` (length `7`) and `beautiful` (length `9`).

### Constraints

- `1 ≤ n ≤ 10^5`
- `1 ≤ length of each string ≤ 100`

### Reference
-GeeksforGeeks – Sort Strings According to Their Lengths

## 8. The Smart Campus Resource Tracker

### Problem Statement

A college is conducting a technical festival where students register every hour. Given an integer array `registrations`, where `registrations[i]` represents the number of students registered during hour `i`, calculate the cumulative total of registrations from the first hour up to each hour and return the resulting running sum array.

### Input Format

- The first line contains an integer `n`, the number of hours.
- The second line contains `n` space-separated integers representing `registrations`.

### Output Format

Print `n` space-separated integers representing the cumulative registrations after each hour.

### Sample Input 1

~~~
5
10 20 15 25 30
~~~

### Sample Output 1

~~~
10 30 45 70 100
~~~

### Sample Input 2

~~~
4
5 8 12 10
~~~

### Sample Output 2

~~~
5 13 25 35
~~~

### Explanation

In sample 1, the cumulative sums are `10`, `10 + 20 = 30`, `30 + 15 = 45`, `45 + 25 = 70`, and `70 + 30 = 100`. In sample 2, the cumulative sums are `5`, `5 + 8 = 13`, `13 + 12 = 25`, and `25 + 10 = 35`.

### Constraints

- `1 ≤ n ≤ 10^5`
- `0 ≤ registrations[i] ≤ 10^6`
- Expected time complexity: `O(n)`; auxiliary space: `O(1)` (excluding output).

### Reference
-LeetCode – Running Sum of 1D Array (Official)
