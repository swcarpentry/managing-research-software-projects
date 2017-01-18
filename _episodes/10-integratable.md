---
title: "Make the Software Easy to Integrate"
teaching: 5
exercises: 10
questions:
- "How can I make it easy for other people to use my software as a component in their work?"
objectives:
- "Explain the pros and cons of command-line parameters vs. configuration files."
- "Explain the pros and cons of libraries vs. external applications."
keypoints:
- "Provide command-line parameters for commonly-changed options."
- "Provide hierarchical configuration files for *all* options."
- "Do not invent your own syntax for configuration files."
---

*   Command-line parameters for commonly-changed options
    *   Also makes program easy to control from shell scripts
*   Configuration files for less frequently changed options
*   Frequently use multiple overlaid configuration files
    *   System-level configuration file created during installation for things like cluster name
    *   User-level configuration file in `~/.programrc` for user's credentials
        *   `rc` suffix is old Unix abbreviation for "resource control"
    *   Job-level configuration file for particular runs
*   Use a standard syntax for configuration files
    *   Windows init files are widely supported
    *   YAML is increasingly popular
    *   "If you have to write a parser, you've done something wrong."
        *   ...or someone upstream from you did
*   How to connect to other programs?
    *   Use a shell script to combine everything: universal but limited
    *   Run your program in a sub-process: ditto
    *   Build a library with a command-line wrapper: flexible, but more work for users

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

> ## Using Your Project as a Component
>
> Suppose someone wants to use your software as part of a larger program
> written in a language other than the one you use.
>
> 1.  What's the simplest way for them to do this?
> 2.  What *won't* they be able to do?
{: .challenge}

{% include links.md %}
