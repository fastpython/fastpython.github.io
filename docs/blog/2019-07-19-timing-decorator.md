---
layout: post
title:  "Time functions with decorator"
date:   2019-07-19 00:00:00 +0300
categories: benchmark profile
---

# Benchmark functions with timing decorator

Who wouldn't want to write own timing decorators? When [wrk](benchmark_with_wrk.md) benchmarking is done and we want to see in more detail how much time our code takes, simple option is add a decorator for your functions we want to measure. 

Hint: If decorators are new to you, there's article [Primer on Python Decorators](https://realpython.com/primer-on-python-decorators/) that gives good overview and see also [Python docs]().

Simple timing decorator could be something like this:

```
from time import time
from functools import wraps

def time_func_call(fn):
    @wraps(fn)
    def wrapper(*args, **kwargs):
        time_start = time()
        result = fn(*args, **kwargs)
        duration = time() - time_start
        print("TIME: {} took {} seconds ({}:{})".format(
            fn.__name__, duration, fn.__code__.co_filename,
            fn.__code__.co_firstlineno))
        return result
    return wrapper
```

And to time your selected function by decorating it:

```
@time_func_call
def generate_response_data():
    ...
```

Resulting output:

```
TIME: generate_response_data took 0.0565491199 seconds (/path/to/file/views.py:123)
```

If you don't mind installing extra packages, there's e.g. [profilehooks](https://github.com/mgedmin/profilehooks) package that is implementing similar functionality among other decorators. 

## Profiling overhead

Yes, this obviously adds some overhead for your code. Overhead might or might not be significant. It depends on the use case. If measuring function execution times with decorator is enough for our profiling purposes, the overhead is most likely not too much especially when it similarly affects all measured functions.

Profiling is almost always causing some overhead. It could be very small if doing statistical analysis without any changes to code or, on the other hand, it can be very huge if doing 

