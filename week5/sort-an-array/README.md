Sort an Array
1. Problem

The task is to sort an array of integers in ascending order. The smallest number should be first, and the largest number should be last.

2. Approach

I used the Quick Sort algorithm. It chooses a pivot element and divides the array into smaller parts.

First, I choose the middle element as the pivot. Then I use two pointers, i and j. Pointer i moves from the left, and pointer j moves from the right.

If an element on the left is greater than or equal to the pivot, and an element on the right is smaller than or equal to the pivot, I swap them when the pointers have not crossed. I continue until the elements are divided into parts. Then I sort each part recursively.

Step-by-step tracing

Input: [5, 2, 3, 1]

The pivot is 2.
The left pointer starts at index 0, and the right pointer starts at index 3.
The left pointer stops at 5, because 5 is greater than the pivot.
The right pointer stops at 1, because 1 is smaller than the pivot.
I swap 5 and 1. The array becomes [1, 2, 3, 5].
The pointers move toward each other and cross. The partition is finished.
The remaining parts are checked recursively. In this example, the array is already sorted.

Output: [1, 2, 3, 5]

Challenges and testing

One challenge was understanding how the two pointers move and when the algorithm should swap elements. I also needed to make sure the recursive calls stop when a part contains zero or one element.

I would test an empty array, an array with one element, an already sorted array, a reverse-sorted array, duplicate values, and an array with negative numbers.

These tests help check that the algorithm handles different inputs correctly.

3. Time and Space Complexity

Time Complexity: O(n log n) on average

The algorithm divides the array into smaller parts. When the partitions are reasonably balanced, there are approximately log n levels of recursion, and each level processes about n elements. Therefore, the average time complexity is O(n log n).

In the worst case, the time complexity is O(n²), for example when partitions become very unbalanced.

Space Complexity: O(log n) on average

Quick Sort uses recursive calls, which require stack memory. With reasonably balanced partitions, the recursion depth is approximately log n. In the worst case, the recursion stack can use O(n) space.

The algorithm sorts the array in place and does not create another array for the elements.

4. Reflection / Improvement

Quick Sort is usually much faster than Bubble Sort for large arrays. However, its worst-case time complexity is O(n²).

One improvement would be to use Heap Sort, which guarantees O(n log n) time and O(1) auxiliary space. Another option is Merge Sort, which guarantees O(n log n) time but usually requires O(n) additional space for arrays.

These algorithms can provide more predictable performance for large inputs.