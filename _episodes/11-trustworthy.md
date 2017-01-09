---
title: "Make the Software Trustworthy"
teaching: 5
exercises: 10
questions:
- "FIXME"
objectives:
- "FIXME"
keypoints:
- "FIXME"
---

*   Not enough to be right - have to be *seen* to be right
*   Include a small test set that can be run to ensure the software is actually working
    *   Not the same as a comprehensive unit test suite for use in development (which you should also have)
    *   Unit tests may take too long to run, and output may not be actionable
    *   Want smaller suite that says "am I set up correctly?"
*   Produce identical results when given identical inputs
    *   Absolutely necessary for reproducible research
    *   Means external control of random numbe generation seeds,
        aggregation order for floating point results,
        dates and times,
        etc.
    *   Probably the hardest thing on this list for many projects

> ## Is This Turned On?
>
> 1.  How can the person who installs your software tell if it is installed correctly?
> 2.  How can the person who *uses* your software tell if it is installed correctly?
{: .challenge}

> ## Out of Control
>
> Under what circumstances could your program produce different answers
> when given what the user believes are the same inputs?
{: .challenge}

{% include links.md %}
