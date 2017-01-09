---
title: "Make the Project Describe Itself"
teaching: 5
exercises: 10
questions:
- "FIXME"
objectives:
- "FIXME"
keypoints:
- "FIXME"
---

*   *Robust* is the difference between "works for me on my machine"
    and "works for someone I've never met on a cluster I've never heard of"
    *   Rules are described in [Taschuk's Rules](http://oicr-gsi.github.io/robust-paper/)
*   Have a README that briefly explains what the software does and what its dependencies are
    *   For humans to read *before* installing
*   Tell the user what could be done
    *   Print usage from the command line by default
    *   Include version (discussed below)
*   Tell the user what was *actually* done
    *   Log actions

> ## Write a Usage Statement
>
> Run `make --help` (or something similar) and examine its output,
> then write a similar command-line usage message for your project.
{: .challenge}

> ## Logging
>
> Read the [tutorial on the Python logging library][python-logging-tutorial]
> (or an equivalent tutorial for your preferred language's logging library).
>
> 1.  How do libraries of this kind give users control over what is logged and where?
> 2.  Is this an appropriate level of complexity for your project?
>     If not, what would you use instead?
{: .challenge}

{% include links.md %}
