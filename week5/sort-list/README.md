Sort List
1. Problem

The task is to sort a singly linked list in ascending order. Each node contains a value and a reference to the next node.

For example:

Input: 4 -> 2 -> 1 -> 3

Output: 1 -> 2 -> 3 -> 4

2. Approach

I used the Merge Sort algorithm. It divides the linked list into smaller parts, sorts them, and merges them back together.

First, I check if the list is empty or contains only one node. If so, the list is already sorted.

Next, I use two pointers to find the middle of the list. The slow pointer moves one step at a time, while the fast pointer moves two steps at a time.

When the fast pointer reaches the end, I split the list into two parts. I sort both parts using recursion and then merge them in ascending order.

Step-by-step tracing

Input: 4 -> 2 -> 1 -> 3

Step 1: Split the list

I divide the list into two parts:

First part: 4 -> 2
Second part: 1 -> 3

Step 2: Sort each part

4 -> 2 becomes 2 -> 4.
1 -> 3 stays 1 -> 3.

Step 3: Merge the sorted parts

I compare the first values of both lists and select the smaller one each time.

Compare 2 and 1. Choose 1.
Compare 2 and 3. Choose 2.
Compare 4 and 3. Choose 3.
Add the remaining value 4.

Final output: 1 -> 2 -> 3 -> 4

Challenges and testing

One challenge was finding the middle of the linked list and splitting it without losing any nodes. Another challenge was merging the two sorted lists in the correct order.

I would test an empty list, a list with one node, an already sorted list, a reverse-sorted list, and a list with duplicate values.

These tests help check whether the algorithm handles different inputs correctly and whether all nodes remain in the final list.

3. Time and Space Complexity

Time Complexity: O(n log n)

The algorithm splits the list into two smaller parts at each recursive level. This creates approximately log n levels. At each level, merging the parts takes O(n) time because each node is processed once.

Therefore, the total time complexity is O(n log n).

Space Complexity: O(log n)

The recursive calls use additional stack memory. Since the list is divided into halves, the recursion depth is approximately log n.

The merge operation reuses the existing nodes instead of creating a new node for every element. The temporary dummy node uses only constant additional space.

4. Reflection / Improvement

Merge Sort is already an efficient algorithm for sorting a linked list.

One possible improvement is to use an iterative, bottom-up Merge Sort instead of recursion. This approach can keep the same O(n log n) time complexity while reducing auxiliary space to O(1), if implemented without allocating additional nodes for the elements.

However, the recursive solution is easier for me to understand and explain.