# Problem Definition

## Description

Given a binary tree, populate an array to represent the **averages of all of its levels**.

Example 1:

```dot
digraph example1 {
    1 -> 2 -> { 4, 5 };
    1 -> 3 -> { 6, 7 };
}
```

```plaintext
Level Order Traversal: [1, 2.5, 5.5]
```

Example 2:

```dot
digraph example1 {
    12 -> 7 -> { 9, 2 };
    12 -> 1 -> { 10, 5 };
}
```

```plaintext
Level Order Traversal: [12.0, 4.0, 6.5]
```

## Discussion

This problem follows the **Binary Tree Level Order Traversal** pattern. We can follow the same **BFS** approach. The only difference will be that instead of keeping track of all nodes of a level, we will only track the running sum of the values of all nodes in each level. In the end, we will append the average of the current level to the result array.

### Time Complexity

The time complexity of the above algorithm is O(N), where āNā is the total number of nodes in the tree. This is due to the fact that we traverse each node once.

### Space Complexity

The space complexity of the above algorithm will be O(N) which is required for the queue. Since we can have a maximum of N/2 nodes at any level (this could happen only at the lowest level), therefore we will need O(N) space to store them in the queue.

## Notes

## References
