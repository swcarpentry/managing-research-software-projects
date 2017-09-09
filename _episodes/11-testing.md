---
title: "Test All The Things"
teaching: 10
exercises: 15
questions:
- "How can I tell if my software is good enough to release?"
- "How can figure out what my code is supposed to do?"
- "How can I stay focused on building what I actually need to?"
objectives:
- "Explain why scientists should think about testing in terms of tolerances."
- "Write unit tests to define what what a simple function is supposed to do."
keypoints:
- "Write tests to define explicit tolerances."
- "Use a unit testing framework to write and run tests."
- "Isolate tests."
---

*   You're already evaluating whether your software does what you think it should do. The question is whether the evaluation process is:
    *   Automated
    *   Comprehensive
    *   Well documented
*   "Physicists worry about decimal places. Astronomers worry about exponents. Economists are happy if they've got the sign right."
    *   I.e., every field of science and engineering has community norms for tolerances
    *   But those community norms don't exist (yet) for software
*   When writing tests, think in terms of tolerances
    *   "What range of outputs will I accept as correct for input X in situation Y?"
*   Integer and text operations: usually require exact answer
*   Anything involving floating point: allow error bars (just as in physical experiments)
    *   But still produce identical answers for identical inputs
*   Examples
    *   When refactoring image processing routine to improve performance:
        if more than 1% of pixels change value by more than the low bit, assume a bug
    *   N-body simulation:
        if system's energy or momentum changes by more than one part in 1.0e6 over lifetime of simulation
        *   Why one in a million?  Because we have to choose something...
*   Types of tests
    *   Smoke tests (does this blow up when I try to use it?)
    *   Unit tests (developers can safely rely on this function to do what it advertises)
    *   Functional tests (users can safely rely on this program to do what it advertises)
    *   Regression tests (make sure this bug never crops up again)
*   Use a unit testing framework to write tests
    *   Each test is a function (or method)
    *   Test results are pass, fail, or error
    *   Optionally run setup before each test and teardown afterward
    *   Test runner finds and runs tests and reports aggregate results
*   Tests should be isolated
    *   Actions of one test should not affect actions of other tests
    *   I.e., should be able to run in arbitrary order with identical results

> ## What Are Your Tolerances?
>
> 1.  What will you measure to determine whether your software is correct enough?
> 2.  What tolerances will you accept on answers?
> 3.  Why?
{: .challenge}

> ## Pick a Unit Testing Framework
>
> 1.  If your project already uses a unit testing framework,
>     explain which one and why you chose it.
> 2.  If your project does not already use a unit testing framework,
>     find one and create one test using it.
{: .challenge}

<blockquote class="challenge" markdown="1">
## First, the Tests

1.  Using `assert` statements,
    write half a dozen tests for each of the following functions.
2.  Compare your tests to those written by your neighbors.
    What errors did they test for that you didn't?
    What would your tests catch that they missed?
3.  Where did you interpret requirements differently?
    I.e., where would a function pass one of your neighbors' tests but fail one of yours
    or vice versa?

{% include problems.md %}
</blockquote>

{% include links.md %}
