---
title: '404 - Oops, this page is no longer here!'
date: 2020-09-12 23:01:35
comments: false
permalink: /404.html
---

<!-- markdownlint-disable MD039 MD033 -->

## This page doesn not exist

Sorry, this page no longer exists.

Will return to home page in <span id="timeout">5</span> seconds.

If you are in a rush, you can **[click here](https://jsonwang95.github.io/)** to return to the home page.

<script>
let countTime = 5;

function count() {
  
  document.getElementById('timeout').textContent = countTime;
  countTime -= 1;
  if(countTime === 0){
    location.href = 'https://jsonwang95.github.io/'; 
  }
  setTimeout(() => {
    count();
  }, 1000);
}

count();
</script>
