Remove Duplicates from Sorted List
1. Problem

The task is to remove duplicate numbers from a sorted linked list.

Each number should appear only once.

Example:

Input: 1 -> 1 -> 2 -> 3 -> 3

Output: 1 -> 2 -> 3

2. Approach

I use a pointer called current to check the nodes in the list.

First, current points to the first node.

I compare the current node with the next node.

If both values are the same, I remove the next node by changing current.next.
If the values are different, I move current to the next node.
I repeat this process until current becomes null.

At the end, I return head, which points to the updated list.

Example / Trace

Input: 1 -> 1 -> 2 -> 3 -> 3

Step 1: The current value is 1, and the next value is also 1. I remove the second 1.

List: 1 -> 2 -> 3 -> 3

Step 2: The current value is 1, and the next value is 2. They are different, so I move to the next node.

Step 3: The current value is 2, and the next value is 3. They are different, so I move forward.

Step 4: The current value is 3, and the next value is also 3. I remove the second 3.

List: 1 -> 2 -> 3

Step 5: There is no next node, so the algorithm finishes.

Output: 1 -> 2 -> 3

Challenges and Testing

One important thing is not moving current after removing a duplicate. There may be more duplicate values next to each other.

I should test different cases:

An empty list.
A list with only one node.
A list with all values the same.
A list without duplicates.
A list with duplicates at the end.

These tests help me check if the code works correctly in different situations.

3. Time Complexity

Time Complexity: O(n)

The algorithm checks the nodes from the beginning to the end of the list. Each step takes a constant amount of time.

If the list has n nodes, the algorithm takes O(n) time.

4. Space Complexity

Space Complexity: O(1)

The algorithm uses only one extra pointer called current. It does not create another list or an array.

The extra memory stays constant even if the list becomes longer.

5. Reflection / Improvement

The solution is already efficient. It takes O(n) time and uses O(1) extra space.

The algorithm checks the list once and does not need additional data structures, so no major improvement is necessary.