Intersection of Two Linked Lists
1. Problem

The task is to find the first common node in two linked lists. If there is no common node, return null.

2. Approach

I use two pointers, a and b.

Pointer a goes through list A. For each node, pointer b checks all nodes in list B.

If a == b, the common node is found, and I return it. If no common node is found, I return null.

Example / Trace

List A: 1 -> 2 -> 8 -> 9

List B: 4 -> 5 -> 8 -> 9

Pointer a checks the nodes in list A.
Pointer b checks the nodes in list B.
When both pointers reach the same node with value 8, the method returns it.
Challenges and Testing

It is important to compare the nodes themselves, not just their values.

I should test lists with an intersection, lists without an intersection, and empty lists.

3. Time Complexity

Time Complexity: O(n * m)

For each node in list A, the algorithm may check every node in list B.

4. Space Complexity

Space Complexity: O(1)

The algorithm uses only two pointers and no extra collections.

5. Reflection / Improvement

A two-pointer approach can improve the time complexity to O(n + m) while keeping O(1) extra space.