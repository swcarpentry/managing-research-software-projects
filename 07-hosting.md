---
title: "Hosting"
teaching: 5
exercises: 10
questions:
- "Where should I host my version control repositories?"
objectives:
- "Explain different options for hosting scientific work."
keypoints:
- "Projects can be hosted on university servers, on personal domains, or on public forges."
- "Rules regarding intellectual property and storage of sensitive information apply no matter where code and data are hosted."
---

*   Where to host code and data?
    *   Privacy
    *   Clear ownership
    *   Availability (uptime, bandwidth, etc.)
*   Option 1:  lab, department, or university provides server, manages accounts and backups, etc.
    *   Pro: clarifies who owns what
        *   Particularly important if any of the material is sensitive
            (i.e., relates to experiments involving human subjects or may be used in a patent application)
    *   Con: cost often higher than commercial services
    *   Con: longevity
        *   Someone who has spent ten years collecting data wants it to be available 10 years from now
        *   That's well beyond the lifespan of most of the grants that fund academic infrastructure
*   Option 2: purchase a domain and pay an Internet service provider (ISP) to host it
    *   Pro: gives the individual or group more control
    *   Pro: sidesteps problems that can arise when moving from one institution to another
    *   Con: requires more time and effort to set up than other options
    *   Con: may not be allowed
*   Option 3: public host service
    *   [GitHub][github], [GitLab][gitlab], [BitBucket][bitbucket], [SourceForge][sourceforge], ...
    *   All provide web interface to
        *   Create, view, and edit projects
        *   Communication and project management tools (issue tracking, wiki pages, email, code reviews)
    *   Pro: economies of scale
    *   Pro: network effects (potential collaborators probably already know how to use them)
    *   Con: public (or only a limited amount of privacy)
        *   Unless you pay
        *   And even then, out-of-institution/out-of-country hosting can be problematic
    *   Con: can be shut down, purchased, etc.

> ## Institutional Barriers
>
> Sharing is the ideal for science,
> but many institutions place restrictions on sharing,
> for example to protect potentially patentable intellectual property.
> If you encounter such restrictions,
> it can be productive to inquire about the underlying motivations
> either to request an exception for a specific project or domain,
> or to push more broadly for institutional reform to support more open science.
{: .callout}

> ## Sharing Code vs. Sharing Publications
>
> Sites like [GitHub][github] are meant for sharing things while they're being developed.
> Services like [arXiV][arxiv] and [figshare][figshare], on the other hand,
> are meant to be used to archive particular snapshots of things for future reference.
> There's obviously overlap between the two -
> in particular, it's possible to tag a particular version of a project in a code repository -
> but as a general rule,
> version control is "where you work"
> while repositories are "where you publish".
{: .callout}

> ## Can My Work Be Public?
>
> Find out whether you are allowed to host your work openly on a public forge.
> Can you do this unilaterally,
> or do you need permission from someone in your institution?
> If so, who?
{: .challenge}

> ## Where Can I Share My Work?
>
> Does your institution have a repository or repositories that you can
> use to share your papers, data and software?
{: .challenge}

{% include links.md %}
