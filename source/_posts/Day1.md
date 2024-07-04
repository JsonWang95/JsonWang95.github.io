---
title: Documenting LeetCode Problems I Solved
date: 2024-05-06 11:33:33
tags:
---

I'll be going over the leetcode 75 questions
<!-- more -->
 (https://leetcode.com/list/?selectedList=pjhln0d2), and hopefully I can do at least two questions a day so it won't take me two months to go over the list. I already solved some of the 75 questions, so I'll be starting from the ones that I haven't tried out yet.

### 121. Best Time to Buy and Sell Stock
![Alt Text](/assets/Leetcode121.png "Problem 121")

### My first approach using two pointers (wrong!)
The first approach that came to my mind was using two pointers; mainly just because that was what I used for the previous problem. The plan was that I would have two pointers to look for the minimum and maximum price in the array, and I would be able to update them accordinly. 
If you think about it, that doesn't really make sense. First of all, those two pointers are basically iterating through the same elements (even though I let one pointer to start at index 0 and the other to start at index 1). The two-pointer approach is useful when they iterate through the array in the opposite direction, which helps reduce the runtime. 
Second, another reason why I wanted to use two pointers was that I could calculate the maximum price difference. However, we can also do that with using just one pointer by marking the minimum and the maximum price along the way.

After analyzing the problem with the wrong approach, it became more clear what we need in our solution. **min_price**, **max_profit**, and just one for loop to iterate through the entire price array. Why don't we need **max_price** here? Well, since we're only using max_price to calculate the max_profit, as we are iterating through the array, we can just do **current_price** - **min_price** and see if that is **max_profit**.

### The correct approach
Here's the qseudocode. First we can checkthe length of the array. Since we can't buy and sell the stock on the same day, we need to have at least two element's in the array. So if the length is less than two, we can simply returm 0.
Next, we set **min_price** to be infinite amd **max_profit** to be 0, and we can update accordingly when we iterate through the array. Finally, just return **max_profit**.

---