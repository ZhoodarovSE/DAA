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

Iteration 1:

Compare 1 and 2.
Since 1 < 2, select 1.
Result: 1

Iteration 2:

Compare 3 and 2.
Since 3 < 2 is false, select 2.
Result: 1 → 2

Iteration 3:

Compare 3 and 4.
Since 3 < 4, select 3.
Result: 1 → 2 → 3

Iteration 4:

Compare 5 and 4.
Since 5 < 4 is false, select 4.
Result: 1 → 2 → 3 → 4

Iteration 5:

Compare 5 and 6.
Since 5 < 6, select 5.
Result: 1 → 2 → 3 → 4 → 5

Final step:

list1 is empty, so attach the remaining node 6.
Result: 1 → 2 → 3 → 4 → 5 → 6

Output:

1 → 2 → 3 → 4 → 5 → 6

3. Time Complexity

Time Complexity: O(n + m)

Each node from both lists is processed at most once. If the lists contain n and m nodes, the total work is proportional to n + m.

4. Space Complexity

Space Complexity: O(1) auxiliary space.

The algorithm uses a fixed number of pointers and one dummy node. It reuses existing nodes instead of creating a new node for every element.

5. Reflection / Improvement

The solution already achieves optimal O(n + m) time complexity because every node may need to be processed. A recursive approach is also possible, but it requires additional call-stack space of up to O(n + m). The iterative approach avoids this overhead.
