---
title: "Test Driven Development"
teaching: 10
exercises: 30
questions:
- "How can figure out what my code is supposed to do?"
- "How can I stay focused on building what I actually need to?"
objectives:
- "Define test-driven development and explain the rationale for it."
- "Write unit tests to define what what a simple function is supposed to do."
keypoints:
- "Test-driven development (TDD) is the practice of writing tests before writing code."
- "Writing tests first helps clarify the intent and interface of the code to be written."
- "Empirical evidence for TDD's benefits is unclear, but many programmers find it very useful."
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
