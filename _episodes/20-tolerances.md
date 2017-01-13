---
title: "Specify Tolerances"
teaching: 5
exercises: 10
questions:
- "How can I tell if my software is good enough to release?"
objectives:
- "Explain why scientists should think about testing in terms of tolerances."
keypoints:
- "Write tests to define explicit tolerances."
- "Use a unit testing framework to write and run tests."
- "Isolate tests."
---

*   "Physicists worry about decimal places. Astronomers worry about exponents. Economists are happy if they've got the sign right."
    *   I.e., every field of science and engineering has community norms for tolerances
    *   But those community norms don't exist (yet) for software
*   When writing tests, think in terms of tolerances
    *   "What range of outputs will I accept as correct for input X in situation Y?"
*   Integer and text operations: usually require exact answer
*   Anything involving floating point: allow error bars (just as in physical experiments)
*   Examples
    *   When refactoring image processing routine to improve performance:
        if more than 1% of pixels change value by more than the low bit, assume a bug
    *   N-body simulation:
        if system's energy or momentum changes by more than one part in 1.0e6 over lifetime of simulation
        *   Why one in a million?  Because we have to choose something...
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

{% include links.md %}
