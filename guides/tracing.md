layout: default
permalink: /guides/tracing
title: Tracing Worksheet
---

# Tracing Worksheet

The ability to trace your code is essential for debugging. Given some arbitrary Python code, you should always be able to answer the questions:

* What line gets executed next?
* What is the current _state_ of memory? In other words, which values are currently assigned to which variables?

## Instructions
Trace the execution of a program by filling in the tables.

1. In __Step__, number the step of execution. Start at line 1 unless otherwise specified. 
2. In __Memory State__, show the values of all variables currently in memory _after_ the line has executed, e.g., `x: 5`
3. In __Next Line__, write down the next line of code that will execute, e.g., 2.
4. In __Output__, write down any text if any, that will be printed.

## Example 1

```python
x = 5
y = 10
sum = x + y
```

{% highlight python linenos %}
x = 5
y = 10
sum = x + y
{% endhighlight %}
