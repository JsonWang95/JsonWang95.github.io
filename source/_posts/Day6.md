---
title: Day 6
date: 2024-06-12 08:57:39
tags:
---
### 347. Top K Frequent Elements
<!-- more -->
![Alt Text](/assets/Leetcode347.png "Problem 347")

### Bucket Sort
For this problem, we'll be using a slightly different version of bucket sort. In convention, when we create a nested array for bucket sort, the length of the outer array would be equal to the length of the array we're sorting. In our case, since the length of the input array could be really big, it's not a good idea to implement it that way (say the input array is [1, 1, 2, 100000], then we would create an array of length 100000, with most of the elements in it being an empty array.)

Thus, we'll create a nested array in a different fashion. The index of the array represents how many times this element appears in the input. The inner array contains the elements that appear that many times. For example, if the input array is [1, 1, 1, 2, 2, 100], our nested array would look like this: [[], [100], [2], [1], [], []].
The reason is that 100 appears one time, so it goes to index 1. 2 appears two times, so it goes to index 2. The benefit of using this data structure is that our array will now be bounded with the length of the input array. If we didn't do it this way, we would've ended up with 100 elements in our array, with most of them being empty. Now we only need six.
After that, we can just go through the inner arrays from the end until we have k elements.