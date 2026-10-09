Binary Search
1. Problem

Given a sorted array of integers nums and an integer target, return the index of the target if it exists. Otherwise, return -1.

2. Approach

My initial approach was linear search with O(n) time complexity. Since the array is sorted, I improved it using binary search.

I initialize left = 0 and right = nums.length - 1. While left <= right, I calculate mid = (left + right) / 2.

If nums[mid] == target, return mid.
If nums[mid] < target, set left = mid + 1.
Otherwise, set right = mid - 1.

If the target is not found, return -1.

3. Time Complexity

Time Complexity: O(log n)

Each iteration eliminates approximately half of the remaining elements. Therefore, the number of iterations grows logarithmically with the array size.

4. Space Complexity

Space Complexity: O(1)

The algorithm uses only three integer variables and does not allocate additional data structures.

5. Reflection / Improvement

Binary search achieves optimal O(log n) time complexity for a sorted array. I could improve the middle index calculation to left + (right - left) / 2 to avoid potential integer overflow.