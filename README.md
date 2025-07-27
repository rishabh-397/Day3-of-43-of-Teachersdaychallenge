# Day3-of-43-of-Teachersdaychallenge
. Top K Frequent Elements
Problem Description: Given an integer array nums and an integer k, return the k most frequent elements.

Approaches Discussed:

Bucket Sort / Frequency Array (O(N) Time Complexity): This highly efficient approach involves two main steps:

Frequency Counting: Use a hash map (std::unordered_map in C++, dict in Python) to count the occurrences of each number.

Bucket Creation: Create an array of lists (or vectors of vectors). The index of this array represents a frequency, and the list at that index contains all numbers that appeared with that specific frequency.

Collection: Iterate through the frequency buckets from the highest possible frequency down to 1. Add numbers to the result list until k elements are collected.

(Alternative: Min-Heap / Priority Queue (O(NlogK) Time Complexity): Another common approach involves using a min-heap to maintain the k elements with the highest frequencies. While valid, the bucket sort method can achieve O(N) on average, which is often faster.)

Key Learning Points:

Leveraging hash maps for efficient frequency calculation.

Understanding and applying the "bucket sort" principle for non-comparison based sorting, specifically by frequency.

Optimizing for linear time complexity by avoiding sorts or heap operations over all N elements when possible.


Invert Binary Tree
Problem Description: Given the root of a binary tree, invert the tree, and return its root. Inverting a tree means swapping the left and right children of every node.

Approaches Discussed:

Recursive Depth-First Search (DFS): This is the most intuitive and elegant solution.

Base Case: If the root is nullptr (empty), there's nothing to invert, so return nullptr.

Recursive Step:

Recursively invert the left subtree.

Recursively invert the right subtree.

Once the children are inverted, swap the root's left and right child pointers.

Return the root.

(Alternative: Iterative BFS/DFS with a Stack/Queue): While recursion is cleaner, this can also be solved iteratively using a stack (for DFS) or a queue (for BFS) to process nodes and swap their children.

Key Learning Points:

Mastering binary tree recursion: defining base cases and the recursive relationship.

Understanding how changes at child nodes propagate up the call stack to affect parent nodes.

The concept of in-place modification of a tree structure.
