---
title: "Packaging"
teaching: 5
exercises: 10
questions:
- "FIXME"
objectives:
- "FIXME"
keypoints:
- "FIXME"
---

*   Describe dependencies in machine-readable form

> ## Requirements for a Simple Website
>
> ~~~
> Django>=1.9,<1.10
> PyYAML
> requests>=2.0
> ~~~
> {: .source}
{: .callout}

*    Set up development machines using a package manager
    *   Doesn't guarantee that the file is up to date, but it helps
*   Use the same package description to install software on users' machines
*   Package managers are often painful to work with
    *   Like standards, everybody has their own
    *   Often language-specific
    *   Often complex (because they're solving complex problems)
    *   Focus on libraries - generally don't address extra development tools

> ## Dependencies
>
> Describe your project's dependencies in the format shown above.
{: .challenge}

{% include links.md %}
