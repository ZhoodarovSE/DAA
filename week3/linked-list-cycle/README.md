Linked List Cycle
1. Problem

Given the head of a linked list, determine whether the list contains a cycle. A cycle exists when following the next pointers eventually leads back to a previously visited node.

2. Approach

I use two pointers, slow and fast, initialized to a dummy node whose next points to the head.

In each iteration, slow moves one node forward, while fast moves two nodes forward. If both pointers meet, the list contains a cycle. If fast or fast.next becomes null, the list has no cycle.

Example Trace

Consider this linked list, where node 4 points back to node 2:

1 → 2 → 3 → 4 → 2 → ...

Step	Slow pointer	Fast pointer
Start	Dummy	Dummy
1	1	2
2	2	4
3	3	3

At step 3, both pointers reach node 3. Therefore, the algorithm returns true.

If the list has no cycle, the fast pointer eventually reaches the end, and the algorithm returns false.

3. Time Complexity

Time Complexity: O(n)

The pointers move through the list at different speeds. If there is no cycle, the fast pointer reaches the end in linear time. If a cycle exists, the pointers meet after at most a linear number of steps relative to the number of nodes.

4. Space Complexity

Space Complexity: O(1) auxiliary space.

The algorithm uses only a dummy node and two pointers. It does not store visited nodes in an additional data structure.

5. Reflection / Improvement

Floyd's cycle detection algorithm already achieves O(n) time and O(1) auxiliary space. A hash set could also detect a cycle, but it would require O(n) additional space. Therefore, the two-pointer approach is more memory-efficient.