---
title: A Slightly Different Halting Problem
layout: default
syntax: true
---
<p class="date">2021-07-22</p>

# Introduction
The halting problem asks whether it's possible to design a function `halts(f)` that
returns `True` if a function `f` halts or `False` if `f` runs forever.

# A Proof That the Halting Problem Is Undecidable
The most common proof that the halting problem is undecidable defines a
program that halts if and only if `halts` says it does not halt:

```python
def liar():
    if halts(liar):
        liar()
```

The idea is that `liar` enters infinite recursion if `halts(liar)` returns
`True`, and `liar` halts if `halts(liar)` returns `False`. It isn't clear
whether `halts(liar)` should return `True` or `False`, so the standard
conclusion is that `halts` cannot exist and thus the halting problem is
undecidable.

# An Analogous Proof
Consider the following proof:

1. Define `positive_or_negative(x)` as a function that takes an integer parameter `x` and returns `True` if `x` is positive or `False` if `x` is negative.
2. Zero is not positive or negative, so `positive_or_negative(0)` can't return either `True` or `False`.
3. The problem of determining whether a number is positive or negative is undecidable.

There are several ways to design a function that determines whether a
number is positive or negative, including:

1. Raise an error on an input of `0`.
2. Return three values instead of a Boolean (possibly `-1` for negative, `0` for zero, and
   `1` for positive).
3. Use an `if-else` construct instead of `if-elif`: define `is_positive` or
   `is_negative` instead of `positive_or_negative`.

The standard proof that the halting problem is undecidable chooses an approach
similar to option 1. I wonder if option 2 or 3 would make more sense.

# Tweaking the Definition of `halts`
The original specification for `halts` looks something like this:

```
def halts(f):
    if f halts:
        return True
    elif f does not halt:
        return False
    else:
        raise an error
```

The analog of option 2 from `positive_or_negative` is to return a different
value for each type of halting behavior, rather than just `True` or `False`.
There are at least five cases to handle: halting programs, infinite
loops, `f` halts if `halts(f)` returns `False`, `f`
halts if `halts(f)` returns `True`, and invalid functions (for example, `f` is a string).

One solution based on option 3 from `positive_or_negative` looks like this:

```
def halts(f):
    if f halts:
        return True
    else:
        return False
```

Here the `else` clause covers all cases other than simple halting, including `liar`.

The question I'd like to raise is whether the standard proof that the halting
problem is undecidable applies to these latter two versions of `halts`.

# Notes
Eric Hehner and Bill Stoddart have raised similar questions in the past. I wrote
a [longer paper](/docs/wyde-halting.pdf) on the halting problem that
looked at Turing's work on the topic, including an incomplete proof of the
`if-else` case in the last paper that he published.

