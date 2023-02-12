---
title: "The Beginner's Guide: Single Threaded & Non-Blocking JS"
author: Elyse Newland
pubDatetime: 2023-02-08T03:42:51Z
postSlug: single-threaded-javascript
featured: false
draft: false
tags:
  - JavaScript
description: "My AHA moment understanding a core Javascript principle."
---

Javascript is a single-threaded language that can be non-blocking.

<video class="w-full h-auto" autoplay loop muted playsinline aria-describedby="video-caption">
    <source src="https://media.giphy.com/media/YVPwi7L2izTJS/giphy.mp4" type="video/mp4">
    <div id="video-caption" class="sr-only">Bubbles, a character from Trailer Park Boys, looking confused.</div>
</video>

**_What?!_**

In Zero To Mastery's [Complete Web Developer Course](https://zerotomastery.io/courses/coding-bootcamp/), I'm learning that this sentence needs to be understood by Javascript developers.

## So what does single-threaded actually mean?

Javascript engines (which run our code in the browser) consist of the memory heap and call stack.

The memory heap is where memory is allocated for our code (e.g., each time we create a variable), while the call stack is where our code is read and executed.

Singled-threaded means that Javascript only has one call stack. Having one call stack means it only runs one thing at a time. This can simplify things compared to multi-threaded languages ( that have multiple call stacks), which can add complexity.

## And what about non-blocking?

Javascript _can_ be non-blocking. Essentially, Javascript says, "Ain't nobody got time for that!"
Javascript doesn't wait around for things that take time, so it performs some tasks asynchronously.

In addition to the Javascript engine, there is also the Javascript run-time environment. This checks a few areas (Web APIs, the callback queue, and the event loop) to ensure the code runs efficiently and quickly. It also consistently checks the call stack to see if it's empty or if there is still code that needs to be executed.

Whew! That took me longer than I want to admit to understand. I'm still working on fully understanding the run-time environment, but I'm closer 😊

Javascript is a single-threaded language that can be non-blocking.

Is it something you understood right away, or did it take time?
