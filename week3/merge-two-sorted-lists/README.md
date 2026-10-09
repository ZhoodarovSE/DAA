Merge Two Sorted Lists
1. Problem

Given two sorted linked lists, merge them into one sorted linked list and return its head.

2. Approach

I use a dummy node to simplify building the result list and a cur pointer to track its last node.

While both lists are not empty, I compare their current values and attach the smaller node to the result. Then I move the corresponding pointer forward and update cur.

When one list becomes empty, I attach the remaining part of the other list to the result.

Example Trace

Input:

list1 = 1 → 3 → 5
list2 = 2 → 4 → 6
Step	Comparison	Result
1	1 < 2	1
2	3 < 2 is false	1 → 2
3	3 < 4	1 → 2 → 3
4	5 < 4 is false	1 → 2 → 3 → 4
5	5 < 6	1 → 2 → 3 → 4 → 5
6	list1 is empty	1 → 2 → 3 → 4 → 5 → 6

Output: 1 → 2 → 3 → 4 → 5 → 6

3. Time Complexity

Time Complexity: O(n + m)

Each node from both lists is processed at most once. If the lists contain n and m nodes, the total work is proportional to n + m.

4. Space Complexity

Space Complexity: O(1) auxiliary space.

The algorithm uses a fixed number of pointers and one dummy node. It reuses existing nodes instead of creating a new node for every element.

5. Reflection / Improvement

The solution already achieves optimal O(n + m) time complexity because every node may need to be processed. A recursive approach is also possible, but it requires additional call-stack space of up to O(n + m). The iterative approach avoids this overhead.