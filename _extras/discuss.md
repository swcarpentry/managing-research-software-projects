---
layout: page
title: Discussion
permalink: /discuss/
---

## When *Not* to Use Version Control

*   You may need to meet people halfway if you want your project to grow
*   In particular, your collaborators might not be using version control
    *   And they might be right
*   Dropbox for files
    *   [Integrates with Git][git-dropbox]
    *   Non-trivial setup...
*   Similarly, they may not use LaTeX or Markdown for papers,
    and may be right there as well
    *   Google Docs for papers

> ...try to explain the notion of compiling a document to an
> overworked physician you collaborate with. Oh, but before that, you
> have to explain the difference between plain text and word
> processing. And text editors. And markdown/LaTeX compilers. And
> BiBTeX. And Git. And GitHub. Etc. Meanwhile he/she is getting paged
> from the OR...
>
> ...as much as we want to convince ourselves otherwise, when you
> have to collaborate with those outside the scientific computing
> bubble, the barrier to collaborating on papers in this framework is
> simply too high to overcome. Good intentions aside, it always comes
> down to "just give me a Word document with tracked changes," or
> similar.
>
> - [Stephen Turner][good-enough]
{: .quotation}

> Google Docs excels at easy sharing, collaboration, simultaneous
> editing, commenting and reply-to-commenting. Sure, one can approximate
> these using text-based systems and version control. The question is
> why anyone would like to...
>
> The goal of reproducible research is to make sure one
> can...reproduce...computational analyses. The goal of version
> control is to track changes to source code. These are fundamentally
> distinct goals, and while there is some overlap, version control is
> merely a tool to help achieve that, and comes with so much overhead
> and baggage that it is often not worth the effort.
>
> [Arjun Raj][quote-raj]
{: .quotation}

> Normal humans don't work like programmers expect them to
> because programmers haven't built tools that would let them.  
>
> - [Mike Hoye][quote-hoye]
{: .quotation}

## Miscellaneous Links

*   Python packaging: <https://glyph.twistedmatrix.com/2016/08/python-packaging.html>
*   Recipy (provenance): <https://github.com/recipy/recipy>
    and <https://www.software.ac.uk/blog/2016-08-15-automated-testing-boost-recipys-confidence>
    *   Lots of other tools like this
    *   None have widespread traction despite their value
*   How to decide what features to build next: <http://mcfunley.com/data-driven-products-now>
*   We're focused on code, but data is just as important
    *   <https://dynamicecology.wordpress.com/2016/08/22/ten-commandments-for-good-data-management/>
*   Containers
    *   Lightweight with `virtualenv`
    *   Medium-weight with Docker
    *   Heavyweight: buy more hardware…
    *   All trying to solve the same problem: stuff evolves
*   How to write a good commit message: <http://chris.beams.io/posts/git-commit/>
*   On being a manager: <https://medium.com/@ednapiranha/want-to-be-an-engineering-manager-74fb6c69d932>
    *   Let go...
*   Terrible clients explained with pirates: <https://toggl.com/worst-client-types-infographic>
*   Kanban stages of grief: <https://twitter.com/rseroter/status/788028797144535040>
*   Simple testing can prevent most critical failures: <https://blog.acolyer.org/2016/10/06/simple-testing-can-prevent-most-critical-failures/>
    *   Leads to <https://www.usenix.org/system/files/conference/osdi14/osdi14-paper-yuan.pdf>
*   How to fund open source projects: <https://github.com/danielskatz/sustaining-research-projects>
*   What is open science? <http://ivory.idyll.org/blog/2016-what-is-open-science.html>

{% include links.md %}
