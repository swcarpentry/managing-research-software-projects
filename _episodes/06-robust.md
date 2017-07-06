---
title: "Make the Software Robust"
teaching: 10
exercises: 15
questions:
- "How can I make it easier for people to find out what my project does?"
- "How can I make it easier for people to install my software?"
- "How can I make it easy for other people to use my software as a component in their work?"
- "How can I convince people that my software is trustworthy?"
objectives:
- "Explain what 'robust software' is."
- "Identify three things projects can do to make themselves easier to understand."
- "Explain what semantic versioning is and why it should be used."
- "Identify two things that can make software hard to install."
- "Explain the pros and cons of command-line parameters vs. configuration files."
- "Explain the pros and cons of libraries vs. external applications."
- "Describe the differences between regression testing and sanity checking."
- "Explain why programs should produce identical output for identical inputs."
keypoints:
- "Robust software is software that works for people you've never met on machines you've never heard of."
- "Every project should have a README that briefly explains its purpose and dependencies."
- "Every program should be able print a short usage message."
- "Every program should be able to log its actions."
- "Use semantic versioning (`major.minor.patch`) to identify software versions."
- "Make old versions of software available."
- "Do not require root permissions or other special privileges to install software."
- "Do not use hard-coded paths in software."
- "Provide command-line parameters for commonly-changed options."
- "Provide hierarchical configuration files for *all* options."
- "Do not invent your own syntax for configuration files."
- "Every application should have a small sanity-testing test suite."
- "Always produce identical results for particular inputs."
---

*   *Robust* is the difference between "works for me on my machine"
    and "works for someone I've never met on a cluster I've never heard of"
    *   Rules are described in [Taschuk's Rules][taschuk-rules]
*   Have a README that briefly explains what the software does and what its dependencies are
    *   For humans to read *before* installing
*   Tell the user what could be done
    *   Print usage from the command line by default
    *   Include version (discussed below)
*   Tell the user what was *actually* done
    *   Log actions by writing messages to a findable place
    *   Use a logging library that allows you to control level of detail
*   Version your releases
    *   Semantic versioning: `major.minor.patch`
    *   Release date versioning: `yyyy.vv`
*   Update the version number every time you release a change (however small)
    *   Tempting not to do a full release when "it was just a little change"
*   Make old versions available
*   Do not require root or other special privileges
    *   Users may have this on their laptop, but probably don't have it on the cluster
*   Eliminate hard-coded paths in the software
    *   `/Users/kermit/run_5/data` probably doesn't exist on other people's machines...
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
*   Not enough to be right - have to be *seen* to be right
*   Include a small test set that can be run to ensure the software is actually working
    *   Not the same as a comprehensive regression test suite for use in development
        *   Which you should also have...
    *   Regression tests may take too long to run, and output may not be actionable
    *   So provide smaller suite that says "am I set up correctly?"
        *   Ideally, also serves as examples of use
*   Produce identical results when given identical inputs
    *   Absolutely necessary for reproducible research
    *   Means external control of random number generation seeds,
        aggregation order for floating point results,
        dates and times,
        etc.
    *   Probably the hardest thing on this list for many projects

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

> ## Is This Turned On?
>
> 1.  How can the person who *installs* your software tell if it is installed correctly?
> 2.  How can the person who *uses* your software tell if it is installed correctly?
> 3.  Where can users find examples of how to run your program?
{: .challenge}

> ## Out of Control
>
> 1.  Under what circumstances could your program produce different answers
>     when given identical inputs?
> 2.  What would you have to change in your program to correct this?
{: .challenge}

{% include links.md %}
