First Bad Version
1. Problem

Given n versions, find the first bad version using the API isBadVersion(version). Once a version is bad, all subsequent versions are also bad.

2. Approach

A linear search would take O(n) time. Instead, I use binary search with left = 1 and right = n.

While left < right, I calculate mid = left + (right - left) / 2.

If isBadVersion(mid) returns true, set right = mid, because mid could be the first bad version.
Otherwise, set left = mid + 1, because the first bad version must be to the right.

When left == right, return left.

3. Time Complexity

Time Complexity: O(log n)

Each iteration halves the search range. Therefore, the algorithm requires logarithmically many iterations and API calls.

4. Space Complexity

Space Complexity: O(1)

The algorithm uses only a fixed number of integer variables and does not allocate additional data structures or use recursion.

5. Reflection / Improvement

The solution already achieves optimal O(log n) time complexity and O(1) auxiliary space. Binary search significantly reduces API calls compared to linear search. The middle index formula also prevents potential integer overflow.