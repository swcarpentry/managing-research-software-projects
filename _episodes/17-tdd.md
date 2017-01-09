---
title: "Test-Driven Development"
teaching: 5
exercises: 10
questions:
- "What is agile software development?"
- "What is sturdy software development?"
- "What kind of development process should my project use?"
objectives:
- "FIXME"
keypoints:
- "FIXME"
---

*   *Test-driven development* (TDD)
    1.  Write a handful of tests that don't even run because the code they
        are supposed to test doesn't exist yet.
    2.  Write just enough code to make those tests pass.
    3.  Clean up what's just been written.
    4.  Commit it to version control.
*   Advocates claim that writing tests first:
    *   Focuses people's minds on what code is supposed to
        so that they're not subject to confirmation bias when viewing test results
    *   Ensures that code actually *is* testable
    *   Ensures tests are actually written
*   Evidence backing these claims is contradictory
    *   Empirical studies have not found a strong positive effect
    *   But many productive programmers believe in it
    *   So maybe we're measuring the wrong things...

> ## First, the Tests
>
> 1.  Using `assert` statements,
>     write half a dozen tests for each of the following functions.
> 2.  Compare your tests to those written by your neighbors.
>     What errors did they test for that you didn't?
>     What would your tests catch that they missed?
> 3.  Where did you interpret requirements differently?
>     I.e., where would a function pass one of your neighbors' tests but fail one of yours
>     or vice versa?
>
> Non-Decreasing Sub-Lists
> :   Given a list of numbers,
>     return a list of the sums of each non-decreasing sub-list.
>     For example,
>     if the input is [1, 2, 3, 3, 1, 5, 6, 3, 1, 2, 3],
>     the output should be [9, 12, 3, 6].
>
> FIXME Second Problem
> :   FIXME spec
{: .challenge}

{% include links.md %}
