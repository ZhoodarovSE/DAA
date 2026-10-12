Palindrome Linked List
1. Problem

The task is to check if a linked list reads the same forward and backward.

Example:

Input: 1 -> 2 -> 2 -> 1

Output: true

2. Approach

First, I copy all values from the linked list into an ArrayList.

Then I use two indexes. One starts at the beginning, and the other starts at the end.

I compare the values. If they are different, I return false. If all values match, I return true.

Example / Trace

Input: 1 -> 2 -> 2 -> 1

Copy the values: [1, 2, 2, 1].
Compare the first and last values: 1 and 1.
Compare the middle values: 2 and 2.
All values match, so the result is true.
Testing

I should test a palindrome, a list that is not a palindrome, a list with one node, and an empty list.

3. Time Complexity

Time Complexity: O(n)

I visit every node and compare the values. The algorithm takes linear time.

4. Space Complexity

Space Complexity: O(n)

I store all node values in an ArrayList, so the extra memory grows with the list size.

5. Reflection / Improvement

A more efficient solution can use O(1) extra space by reversing the second half of the linked list. The time complexity would remain O(n).