---
title: Day 5
date: 2024-06-09 00:33:23
tags:
---
### 70. Climbing Stairs
<!-- more -->
![Alt Text](/assets/Leetcode70.png "Problem 70")

### Dynamic Programming
Thanks to Neetcode(a youtuber who has many leetcode tutorials), this problem became much easier to break down and understand. Using dynamic programming, we can actually turn this problem into a Fibonacci sequence problem. FIrst, let's visualize the sairs in our head. When n = 3, it means the stair has three steps. Now, we have a few ways to get to the top. We take 1 step + 1 step + 1 step, 1 step + 2 steps, and 2 steps + 1 step.

We can also visualize the process by drawing out a tree. At the root, we have 0. Let's say n = 5. Going from 0, we have two choices of taking the step, either we take 1 step or 2 steps. At each level, we will always only have those two choices. So our tree would be something like this:
                  0
               /     \
              1        2   <-
             / \       /  \
       ->   2   3 <-> 3    4 
           /\   /\   /\    / \
         3   4  4 5  4 5  5   6
        / \  /\ 
       4  5  5  6
      /
     5

Note that I didn't actually finish the tree, but you can see that we are solving the same subprolmes(arrow signs). Right now, the time complexity of this solution would be 2^n. Because we have two options at each level, and the height of the tree is roughly going to be the longest path, so the time complexity is 2^5 here.

Obviously that is not the optimal solution. Since we're solving the same subproblem in the tree, we can get rid off the duplicated part and only calculate the necessary section. After taking out the unnecessary part, we'll get a O(n) solution, since we only have to do a depth first search on the left most path (which will give us enough information to complete the rest of the tree).

At this point, we are pretty much solving a dynamic programming problem. As we're doing DFS to traverse down the tree, we'll hit the base case at the leaf node. For the rest of the solution, I believe it's best to draw out a diagram to see how this can be turned into a Fibonacci sequence problem. Here is the link to the turorial I watched. https://www.youtube.com/watch?v=Y0lT9Fck7qI 