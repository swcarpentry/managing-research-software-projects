---
title: "Automate Development Tasks"
teaching: 5
exercises: 10
questions:
- "How should I handle tasks I do repeatedly?"
objectives:
- "Explain what build managers were originally designed to do, and what else they are now used to do."
- "Make a build file self-explaining."
keypoints:
- "Use a build manager to manage repetitive tasks."
- "Make build files explain themselves."
---

*   DRY: Don't Repeat Yourself
    *   Usually applied to nouns (code)
    *   Just as true for verbs (actions)
    *   The only thing you can accomplish by typing something repeatedly is to get it wrong
*   Use a build manager
    *   [GNU Make][gnu-make] defined the category, but depends on native shell commands
    *   [CMake][cmake] is a meta-tool that creates build files for multiple systems
    *   [SCons][scons] and similar tools define build rules in a full-blown programming language
*   Originally created to compile multi-file programs efficiently, but can all be used for arbitrary tasks
    *   Run tests, build packages for release, create reports, ...
    *   Common pattern: build shell script or utility program, then launch from build file
*   Key feature: dependencies
    *   "X depends on Y depends on Z"
    *   Usually implemented using timestamps or hashes
    *   Not well suited to verbs
*   General workflow tools may be a better fit for actual scientific work
    *   [Galaxy][galaxy] is a high-end tool
    *   [doit][pydoit] is a lot easier to start with

> ## Create a Task list
>
> 1.  If your project already uses a build manager,
>     what tasks are used most often?
> 2.  If your project *doesn't* use a build manager,
>     what are the first few tasks you should automate?
{: .challenge}

> ## Self-Documenting Build Files
>
> The default target in a build file (e.g., `make` with no parameters)
> should print a list of available commands.
> Look at the `Makefile` in this repository to see how this works,
> then modify the build file for your project to do so as well.
{: .challenge}

{% include links.md %}
