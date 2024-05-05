---
title: Setting Up A Personal Blog With Hexo (Small nuance problems you might run into)
date: 2024-05-04 11:29:30
tags:
---

As an aspiring software engineer, I believe it's crucial to have my own personal website to showcase my projects.

<!-- more -->
However, every time I sat down to start building it, I got distracted by the many features I wanted to include. After reading a book called "Atomic Habits"—which I believe many people have heard of—I decided to start with a smaller goal. I came across a few tutorials on building a blog with a simple tool called "Hexo", and it seemed like a good starting point. Hexo is really simple to set up, and I'll cover a few common problems you might encounter, along with some helpful tips.

### 1. Deploying Your Website to GitHub
When deploying your website to GitHub, you need to modify the `_config.yml` file located in the root directory. You'll need to specify the `type`, `repo`, and `branch`. Most tutorials suggest setting the `branch` to "master". However, this can lead to issues because GitHub has changed the default branch name to "main". If you set the `branch` to "master", you might find that your Hexo files are not being pushed to the main branch, which means your updates won't appear on your website. While the topic of branches is extensive, for our purposes, there isn't much difference between the "main" and "master" branches.

**TL;DR:**
Ensure you set the `branch` to "main" to avoid any issues.

### 2. Understanding the `hexo clean` Command
The tutorials often mention the command `hexo clean`, explaining only that it clears all cache and the static pages that were generated. This explanation was confusing to me at first. Essentially, `hexo clean` is a command that resets and cleans up your development environment. Think of it this way: most people use Hexo to build a blog, right? During the building process, every time you open a file, Hexo creates several other files under the hood. If you decide to delete some older posts, the related files might still linger. Here's where `hexo clean` becomes useful—it's considered good practice to run it before posting something new to keep your project tidy and organized.

Also, yes, it's safe to run this command at any time, and it won't accidentally delete any of your posts.


### 3. Finishing up the github setup
If you follow the tutorials, you should be able to have the basic funtions of your hexo site working, which is publishing posts and updating them. However, you might have noticed that not all your files are being pushed to your github repo. Why is that the case? Didn't we create a github repo and update the deployment setting in the `_config.yml`file? In fact, by doing so, we're only partially done with the github setup. When we run `hexo deploy`, we're only pusing the generated static files in the `public` directory. Thus, we still have to do the git commands on our own should you wish to have them all on your github repo. 

---