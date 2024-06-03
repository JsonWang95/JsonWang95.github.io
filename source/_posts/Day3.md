---
title: Day3
date: 2024-05-15 16:30:21
tags:
---
### 226. Invert Binary Tree
<!-- more -->
![Alt Text](/assets/Leetcode226.png "Problem 226")

### Invert with recursion
To solve this problem, we're going to use two concepts that are pretty common for leetcode quetions. First, we're going to use recursion to go all the way down to the leaf nodes of the tree. Second, we're going do the swapping by using `temp` to hold the node values temporarily.

Here's the pseudocode. We first define our base case; when the root node is null, we return. Next, we do the swapping. Finally, we call the recursive functions on both children of the root.