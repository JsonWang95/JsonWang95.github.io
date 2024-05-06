---
title: One LeetCode A Day Until I Land A SWE Job - Day 1
date: 2024-05-06 11:33:33
tags:
---

I've been going on and off LeetCode over the past two years or so after I graduated from college. However, that's not gonna get me anywhere.
<!-- more -->
To be able to really be good at leetcode, I believe I have to be a lot more consistent and practice it evert single day. Previously, the way I did it was that I picked a question, stared at it for a while, realized I couldn't finish it on my own, looked up some solutions/videos, and pretended I actually knew how to solve it. 

This time, I want to make sure that I write down my entire thought process so that I know what my weaknesses are. I'll be going over the leetcode 75 questions (https://leetcode.com/list/?selectedList=pjhln0d2), and hopefully I can do at least two questions a day so it won't take me two months to go over the list. I already solved some of the 75 questions, so I'll be starting from the ones that I haven't tried out yet.

### 1. Deploying Your Website to GitHub
When deploying your website to GitHub, you need to modify the `_config.yml` file located in the root directory. You'll need to specify the `type`, `repo`, and `branch`. Most tutorials suggest setting the `branch` to "master". However, this can lead to issues because GitHub has changed the default branch name to "main". If you set the `branch` to "master", you might find that your Hexo files are not being pushed to the main branch, which means your updates won't appear on your website. While the topic of branches is extensive, for our purposes, there isn't much difference between the "main" and "master" branches.

**TL;DR:**
Ensure you set the `branch` to "main" to avoid any issues.

### 2. Understanding the `hexo clean` Command
The tutorials often mention the command `hexo clean`, explaining only that it clears all cache and the static pages that were generated. This explanation was

---