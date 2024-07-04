---
title: Day4
date: 2024-05-23 23:39:38
tags:
---
### 20. Valid Palindrome
<!-- more -->
![Alt Text](/assets/Leetcode20.png "Problem 20")

### Stack Data Structure
We'll be using stack data structure for this problem. Stack is perfect for this problem because of its last-in-first-out property, as opposed to that of a heap. We will take a look at an example to see how stack is especially useful here.
Say we've got an input `()[()]`. First, we want to have a way to know how the parentheses are paired up. That is, `(` should be matched with `)`. Thus, we can have a dictionary like this, `closeToOpen = {")" : "(", "]" : "[", "}" : "{"}`. Note that we can also do `openToClose`, but it's going to be a bit less intuitive when we  write out the solution.

Now that we have the dictionary, we can iterate through the input array. We first check if the current character `c` is in the dictionray. If it is, it means it's a closing bracket (when we do `if c in closeToOpen`, it's checking for the keys in the dictionary, not the values.) We then check if the element on the top of our stack is the corresponding opening bracket. If they match, we pop out the top element; otherwise, we have an invalid pair and return false right away.

If `c` is not in the dictionary, it means that it is a opening bracket, and we can simply add it to our stack.

When I first attempted this question, I got stuck trying to think if there could be a case where we have a very complicated and nested pairs of parentheses. I thought that there might be a case where we missed some valid/invalid paranthese. However, if you think about it, there centainly could be multiple nested parentheses, but each of those instances will still have the inner-most parentheses. Our solution can still ensure that we look at those inner-most pairs.