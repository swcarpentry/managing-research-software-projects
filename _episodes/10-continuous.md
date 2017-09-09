---
title: "Continuous Integration"
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
        *   [pep8][pep8] for Python
        *   [formatR][formatR] for R
    *   Most are configurable
        *   Stick to a pre-defined style rather than argue about one of your own
    *   Automatic enforcement eliminates subjective arguments
        *   If the linter passes, the code is approved
        *   Guarantees you never have to worry about style if the linter is happy
        *   Most linters support exceptions, these can be approved in code review on a case-by-case basis

> ## Lint Your Code
>
> 1.  Find and install a [lint][lint]-like tool for your preferred language and run it on your code.
> 2.  What does it complain about?
> 3.  Which of its complaints do you disagree with?
{: .challenge}

> ## Setting Up Continuous Integration
>
> Follow the steps in [this tutorial][python-travis-tutorial] to set up Travis-CI testing for the SNDS repository.
> How long did it take you to set this up?
{: .challenge}

{% include links.md %}
