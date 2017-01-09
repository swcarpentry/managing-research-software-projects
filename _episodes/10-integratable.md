---
title: "Make the Software Easy to Integrate"
teaching: 5
exercises: 10
questions:
- "FIXME"
objectives:
- "FIXME"
keypoints:
- "FIXME"
---

*   Command-line parameters for commonly-changed options
    *   Also makes program easy to control from shell scripts
*   Configuration files for less frequently changed options
*   Frequently use multiple overlaid configuration files
    *   System-level configuration file created during installation for things like cluster name
    *   User-level configuration file in `~/.programrc` for user's credentials
        *   `rc` suffix is old Unix abbreviation for "resource control"
    *   Job-level configuration file for particular runs

> ## Common and Rare
>
> 1.  What options or parameters does your program use?
> 2.  Which ones are users most likely to set or change?
> 3.  How do you know?
{: .challenge}

> ## Configuration Files
>
> 1.  Can some or all of your program's options be specified in an external configuration file?
> 2.  If so, what data format do those files use?
> 3.  If not, is it worth adding that capability?
{: .challenge}

{% include links.md %}
