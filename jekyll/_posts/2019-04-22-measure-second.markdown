---
layout: post
title:  "Measure second"
date:   2019-04-22 01:23:45 +0300
categories: start-with-this
---

>
> <span style="color: #0e103a;"> \[me\] Alright, I have my tests to cover my back... </span>
>
> <span style="color: #15873f;"> \[guru\] Yes. And then you'll measure if you really know what your code is doing. </span>
>

Before you'll do any optimization, you need to really understand what your code is doing.

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

The last one is something you need to keep in mind always though not really help optimizing for faster code. It's important to remember that the code should be maintainable even after optimization. It doesn't help much if you today optimize your code to be blazing fast, but tomorrow nobody can maintain it and your app falls apart. 

To write that as a more simple list it would be:

```
Know your software:
    1. Measure performace
    2. Profile to understand better
    3. Data structures
```
