---
title: "Organize Deliberately"
teaching: 5
exercises: 5
questions:
- "How should I organize my research software project?"
objectives:
- "Explain Noble's rules and emphasize the principle of organizing and naming files to reflect their content or purpose."
keypoints:
- "Name each project component (code, data, metadata, etc.) according to its content or purpose."
- "Group similar project files into dedicated directories."
- "Take advantage of widely used project organization conventions unless there is a compelling reason not to."
---

## Project organization

*   Project organization is like a diet
    *   There is no such thing as "no diet", you're "dieting" whether it's intentional or not; it's either a *good* diet or a *poor* diet
    *   Similarly, there is no such thing as "no project organization"; your project is either organized *well* or organized *poorly*
*   An example: Noble's rules
    *   Based on [this paper](http://dx.doi.org/doi:10.1371/journal.pcbi.1000424)
    *   Code in `src/`, raw data in `data/`, programs in `bin/`, documentation and/or manuscripts in `doc/`, etc.
*   This isn't the *only* way to organize research software projects. What principles can we generalize?
    *   Name files according to their content or purpose.
    *   Group similar files together in appropriately named directories.
    *   Take advantage of naming and organization conventions unless there is a compelling reason to "roll your own".

> ## How Is Your Project Currently Organized?
>
> Draw a diagram of how your project is currently organized?
> - Is this documented anywhere?
> - Would it be intuitive for a newcomer?
> - Are there any changes you could make to take advantage of common conventions?
{: .challenge}

{% include links.md %}
