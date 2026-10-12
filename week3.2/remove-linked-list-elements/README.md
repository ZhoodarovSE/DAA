Remove Linked List Elements
1. Problem

The task is to remove all nodes with a given value from a linked list.

Example:

Input: 7 -> 2 -> 7 -> 3, val = 7

Output: 2 -> 3

2. Approach

First, I remove nodes with the target value from the beginning of the list.

Then I use a pointer called current to check the other nodes. If the next node has the target value, I skip it. Otherwise, I move to the next node.

Finally, I return the updated head.

Example / Trace

Input: 7 -> 2 -> 7 -> 3, val = 7

Remove the first node with value 7.
The list becomes 2 -> 7 -> 3.
Skip the next node with value 7.
The list becomes 2 -> 3.

Output: 2 -> 3

Testing

I should test an empty list, a list with no matching values, and a list where all nodes have the target value.

3. Time Complexity

Time Complexity: O(n)

The algorithm checks each node at most a constant number of times.

4. Space Complexity

Space Complexity: O(1)

The algorithm uses only one extra pointer and does not create another list.

5. Reflection / Improvement

The solution is already efficient. It takes O(n) time and uses O(1) extra space.