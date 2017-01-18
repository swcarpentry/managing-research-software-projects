---
title: "Work While You're Asleep"
teaching: 5
exercises: 10
questions:
- "How can I tell what state my project is actually in?"
objectives:
- "Explain how continuous integration works."
- "Configure continuous integration for a small software project."
keypoints:
- "Continuous integration rebuilds and/or re-tests software every time something changes."
- "Use continuous integration to check changes before they are inspected."
- "Check style as well as correctness."
- "Adopt a widely-used pre-defined coding style rather than inventing one of your own."
---

*   *Continuous integration*:
    *   Build and test code every time someone commits code
    *   Post results somewhere the team can see them
    *   If build or tests fail, send out notifications
*   Even better: build and test changes *before* they're merged
    *   Only do code review on changes that have passed mechanical checks
*   Keep track of test coverage
    *   Which parts of the code are being exercised and which aren't
    *   Many different ways to measure
    *   Most important measurement is "are we holding steady?"
*   Most widely used system is [Travis CI][travis-ci]
    *   Easy integration with [Github][github]
    *   Will run tests on multiple platforms and with multiple versions of tools
*   Developers still have to build the tests
    *   CI only as good as the tests it runs
*   Check style as well as correctness
    *   Sometimes called "linters" after the original [lint][lint] for C
    *   Equivalents have been built for most languages
        *   E.g., [pep8][pep8] for Python
    *   Most are configurable
        *   Stick to a pre-defined style rather than argue about one of your own

> ## Lint Your Code
>
> 1.  Find and install a [lint][lint]-like tool for your preferred language and run it on your code.
> 2.  What does it complain about?
> 3.  Which of its complaints do you disagree with?
{: .challenge}

> ## Setting Up Continuous Integration
>
> 1.  Create a new Git repository on GitHub
>     and add a single Python file with one function that adds two numbers.
> 2.  Follow the steps in [this tutorial][python-travis-tutorial]
>     to set up Travis-CI testing of that function.
>
> How long did it take you to set this up?
{: .challenge}

{% include links.md %}
