---
title: "Distribute Your Software"
teaching: 5
exercises: 10
questions:
- "How should I package my software for release?"
objectives:
- "Explain how and why to describe software dependencies in machine-readable form."
- "Explain why development machines should always be set up using package descriptions."
keypoints:
- "Every software ecosystem now includes a package manager to track and update dependencies."
- "Describe software versions in precise machine-readable form to take advantage of these."
- "Always set up development machines using the package description in order to ensure it's up to date."
---

*   Package managers support software installation with a single command
    *   Handle dependencies recursively
    *   Easily scripted/automated
*   Motivation: ease software installation burden
    *   For users and sysadmins at least
    *   Result: a bit more work for the developer(s)
*   Describe project dependencies in machine-readable form
    *   E.g., Python's `requirements.txt` gives package names, and optionally (ranges of) versions

> ## Requirements for a Simple Website
>
> This `requirements.txt` file specifies that a website needs Django version 1.9.something,
> any version of PyYAML,
> and Version 2.0 or later of the requests library.
> Running `pip install -r requirements.txt` on the command line
> will find and install this software.
>
> ~~~
> Django>=1.9,<1.10
> PyYAML
> requests>=2.0
> ~~~
> {: .source}
{: .callout}

*   Common package managers
    *   OS-specific: homebrew, apt, yum, pacman
    *   Language-specific: pip, cran, npm, gem, cpan
    *   Generic: conda, others?
*   Set up development machines using a package manager
    *   Doesn't guarantee that the file is up to date, but it helps
*   Use the same package description to install software on users' machines
*   Package managers are often painful to work with
    *   Like standards, everybody has their own
    *   Often language-specific
    *   Often complex (because they're solving complex problems)
    *   Focus on libraries - generally don't address extra development tools

> ## Ask Your Doctor: Is Packaging Right for You?
>
> 1.  What language is your project primarily implemented in?
>     Does a package manager exist for this language?
> 2.  Write down your project's dependencies.
>     Can these be installed with a package manager?
>     Is this the same package manager as above?
> 3.  How do you know if your dependency list is correct?
>     How would you know if something changed and it fell out of date?
{: .challenge}

{% include links.md %}
