---
layout: post
title:  "Always think first"
date:   2019-04-15 01:23:45 +0300
categories: start-with-this
---

>
> <span style="color: #0e103a;"> \[me\] Yes, so how to optimize my code? </span>
>
> <span style="color: #15873f;"> \[guru\] So, you want to start optimizing your code? Hold on a minute! Are you sure you really know what you want to achieve? </span>
>

Unfortuntaly, there are (currently) no shortcuts or magic buttons you could click to make your Python code perform faster.

It's not a good idea to apply any optimization patterns and hope you get improvements. Don't assume anything. By making assumptions and optimizing your code accordingly with different tweaks you might some day get lucky and get results, but probably you won't. And, meanwhile, you most likely sooner or later would just break your code somehow. 

There are steps you need to take before optimizing anything. Good guideline to follow is that _always understand what you are trying achieve_. Optimizing blindly is a disaster waiting to happen.

It's easy an list to remember:

```
Prepare:
    1. Tests
    2. Targets
    3. Hypothesis
```

So, that do those points means; you need to prepare and think first:

1. Make sure your automatic tests cover the feature your are going to optimize
    - If optimizing code you are not testing, it's only a matter of time you'll break something
    - This is important part. Don't continue until you have tests for your code.

1. Set targets for your optimization
    - If you don't know when to stop, you'll keep tweaking this and that until the end of the world
    - Also, it's worth considering what is acceptable as "fast" and not acceptable as "slow"

1. Form a hypothesis for why your code is slow
    - You won't most likely get everything right, but it's a good learning excerise
    - Do this before you prove yourself right or wrong with measurements and profiling

Now you have some idea on what you want to achieve and what - in your opinion - should be the problem with your slow API end-point. 
