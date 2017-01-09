---
title: "Make the Project Installable"
teaching: 5
exercises: 10
questions:
- "FIXME"
objectives:
- "FIXME"
keypoints:
- "FIXME"
---

*   Version your releases
    *   Semantic versioning: `major.minor.patch`
    *   Release date versioning: `yyyy.vv`
*   Make old versions available
*   Do not require root or other special privileges
*   Eliminate hard-coded paths in the software

> ## How Do You Version Now?
>
> How many different versions of your project are in use right now?
> How do you know?
> If a user has a problem,
> how will you and they find out which version of the software they have?
{: .challenge}

> ## Where Does Your Software Live?
>
> 1.  What directories does your software add files to when it is installed?
> 2.  What new directories does it create?
{: .challenge}

> ## Hard-coded Paths
>
> 1.  What files does your software read and/or write?
> 2.  How do you know?
> 3.  Which of these are referenced by fixed (hard-coded) paths?
{: .challenge}

{% include links.md %}
