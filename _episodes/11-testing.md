---
title: "Specify Tolerances"
teaching: 5
exercises: 10
questions:
- "How can I tell if my software is good enough to release?"
- "How can figure out what my code is supposed to do?"
- "How can I stay focused on building what I actually need to?"
objectives:
- "Explain why scientists should think about testing in terms of tolerances."
- "Define test-driven development and explain the rationale for it."
- "Write unit tests to define what what a simple function is supposed to do."
keypoints:
- "Write tests to define explicit tolerances."
- "Use a unit testing framework to write and run tests."
- "Isolate tests."
- "Test-driven development (TDD) is the practice of writing tests before writing code."
- "Writing tests first helps clarify the intent and interface of the code to be written."
- "Empirical evidence for TDD's benefits is unclear, but many programmers find it very useful."
---

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
*   Use a unit testing framework to write tests
    *   Each test is a function (or method)
    *   Test results are pass, fail, or error
    *   Optionally run setup before each test and teardown afterward
    *   Test runner finds and runs tests and reports aggregate results
*   Tests should be isolated
    *   Actions of one test should not affect actions of other tests
    *   I.e., should be able to run in arbitrary order with identical results
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
