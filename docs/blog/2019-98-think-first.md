---
layout: post
title:  "Always think first"
date:   2019-08-16 00:00:00 +0300
categories: benchmark profile
---

>
> <span style="color: #0e103a;"> \[dev\] Yes, so how to optimize my code? </span>
>
> <span style="color: #15873f;"> \[guru\] So, you want to start optimizing. Hold on a minute! Are you sure you know what your code is doing? </span>
>

Unfortuntaly, there are (currently) no shortcuts or magic buttons you could click to make your Python code perform faster.

It's not a good idea to apply any optimization patterns and hope you get improvements. Don't assume anything. By making assumptions and optimizing your code accordingly with different tweaks you might some day get lucky and get results, but probably you won't. And, meanwhile, you most likely sooner or later would just break your code somehow. 

There are steps you need to take before optimizing anything. Good guideline to follow is that _always understand what you are trying optimize_. Optimizing blindly is disaster waiting to happen.

**Steps before anything else:**

1. Make sure your automatic tests cover the feature your are going to optimize
    - If optimizing code you are not testing, it's only a matter of time you'll break something
    - This is important part. Don't continue until you have tests for your code.

1. Set targets for your optimization
    - If you don't know when to stop, you'll keep tweaking this and that until the end of the world
    - Also, it's worth considering what is acceptable as "fast" and not acceptable as "slow"

1. Form a hypothesis for why your code is slow
    - You won't most likely get everything right, but it's a good learning excerise
    - Do this before you prove yourself right or wrong with measurements

Now you have some idea what you want to achieve and what - in your opinion - is the problem with your slow API end-point. 


### Steps before starting to optimize

1.  Measure the baseline for the performance
    - Time the function or e.g. API end-point
    - Consider timing a single request and multiple parallel requests

1. Profile the code you are trying to optimize
    - Find out what role different parts of the code play in your measurements
    - Is your code running slow (CPU, memory) or waiting something (IO)
    - Find on code line level what is slow and what is not

1. Based on profiling think about the data structures
    - Are you using data structures as they should be used?
    - How is your data strucure 

1. Remind yourself that code maintainability is important factor when optimizing


When you have ticked those steps done, you should have an idea what actually should be optimized.
