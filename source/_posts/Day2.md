---
title: Day2
date: 2024-05-08 20:44:37
tags:
---

### 206. Reverse Linked List
<!-- more -->
![Alt Text](/assets/Leetcode206.png "Problem 206")

### Understanding linked list data structure
Before we solve the problem, I think it's important to understand the data structure of a linked list. As stated in the question, we're working with a singly linked list, meaning that each node has a pointer that points to the next node. Thus, if you have access to the head node, you have access to the entire linked list. One more thing to note is that the last node of a linked list will be pointing to null.

### Doing a small trick to reverse the linked list
Here's what we're gonna do. We'll look at two nodes at a time, and we'll reverse the direction of the pointer. However, to be able to do that we're gonna need an extra pointer to point at the next node. Now, if you take a look at the example up there, when we reverse the pointer that goes from node 1 to node 2, you lose access to node 2, which is why we need an extra pointer to store that.

Now that we have everything we need, we can start to go through the linked list and reverse the pointers. We'll mainly be working with three things: `prev`, `curr`, and `temp`. First, `prev` will be referencing to `null`, whose `next` will be pointing to the head of the linked list. `curr` will be referencing to the head, and `temp` will be referencing to `next` of `curr`.

Here's the order of the actual reversing step. First, we store `next` of the head at `temp`. We then make `next` of the head to be `prev`. At this point, the reverse is complete. We then move `prev` and `curr` to the next element in the linked list. We'll continue to do this until `curr` becomes `null`, which means `prev` will be referencing to the original last node of the linked list. Finally, since we've reversed the entire linked list, the original last node has now become the new `head`. Thus, we can return `prev` and it will give us the answer.

