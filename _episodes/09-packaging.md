---
title: "Packaging"
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

*   Set up development machines using a package manager
    *   Doesn't guarantee that the file is up to date, but it helps
*   Use the same package description to install software on users' machines
*   Package managers are often painful to work with
    *   Like standards, everybody has their own
    *   Often language-specific
    *   Often complex (because they're solving complex problems)
    *   Focus on libraries - generally don't address extra development tools

> ## There Was a Better Way
>
> Rather than relying on human beings to update version numbers appropriately as software changes,
> a method called *design by contract* relies on precise specifications of what functions do
> in order to determine whether an upgrade will break existing behavior.
> Unfortunately, design by contract has never become widespread.
{: .callout}

> ## Dependencies
>
> 1.  Describe your project's dependencies in the format shown above.
> 2.  How do you know the list is correct?
>     How would you know if something changed and it fell out of date?
{: .challenge}

{% include links.md %}
