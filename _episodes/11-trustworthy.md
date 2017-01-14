---
title: "Make the Software Trustworthy"
teaching: 5
exercises: 10
questions:
- "How can I convince people that my software is trustworthy?"
objectives:
- "Describe the differences between regression testing and sanity checking."
- "Explain why programs should produce identical output for identical inputs."
keypoints:
- "Every application should have a small sanity-testing test suite."
- "Always produce identical results for particular inputs."
---

*   Not enough to be right - have to be *seen* to be right
*   Include a small test set that can be run to ensure the software is actually working
    *   Not the same as a comprehensive regression test suite for use in development
        *   Which you should also have...
    *   Regression tests may take too long to run, and output may not be actionable
    *   So provide smaller suite that says "am I set up correctly?"
        *   Ideally, also serves as examples of use
*   Produce identical results when given identical inputs
    *   Absolutely necessary for reproducible research
    *   Means external control of random number generation seeds,
        aggregation order for floating point results,
        dates and times,
        etc.
    *   Probably the hardest thing on this list for many projects

> ## Is This Turned On?
>
> 1.  How can the person who *installs* your software tell if it is installed correctly?
> 2.  How can the person who *uses* your software tell if it is installed correctly?
> 3.  Where can users find examples of how to run your program?
{: .challenge}

> ## Out of Control
>
> 1.  Under what circumstances could your program produce different answers
>     when given identical inputs?
> 2.  What would you have to change in your program to correct this?
{: .challenge}

{% include links.md %}
