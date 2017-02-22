---
title: "Automate Development Tasks"
teaching: 10
exercises: 20
questions:
- "How should I handle tasks I do repeatedly?"
- "How should I handle tasks that need to be done repeatedly, but computers can't do automatically?"
objectives:
- "Explain what build managers were originally designed to do, and what else they are now used to do."
- "Make a build file self-explaining."
- "Explain when to use checklists rather than a build manager."
keypoints:
- "Use a build manager to manage repetitive tasks."
- "Make build files explain themselves."
- "Use checklists for tasks that have to be done repeatedly, but can't be done by a computer."
- "Have new contributors go through checklists to look for omissions and inaccuracies."
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
    *   Only as stable as the pieces they connect
*   A checklist is a build file meant to be executed by human beings
    *   *[The Checklist Manifesto][gawande-checklist-manifesto]*
        describes how use of checklists cuts fatalities in surgery significantly,
        along with many other examples
*   Use them for anything that *can't* be done automatically by a machine
*   Keep in version control
    *   Ask every new contributor/user to use *and give feedback*
*   Include a contact email address in every checklist

> ## Checklist for First Day of Software Carpentry Workshop
>
> 1.  As learners arrive,
>     ask them to connect to the network
>     and check that they have software installed.
> 2.  Remind everyone of the Code of Conduct.
> 3.  Circulate the sign-in sheet and photo release form.
> 4.  Distribute sticky notes.
> 5.  Debug remaining software installation problems.
>     *   If someone can't get software working, pair them with someone who has it working.
> 6.  Remind learners of the workshop's goals and schedule.
> 7.  Remind helpers to mingle as well as answer questions.
>
> Questions or suggestions? Email help@software-carpentry.org.
{: .callout}

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

> ## Create a Setup Checklist
>
> 1.  Write a short point-form checklist describing the things you do
>     when setting up a new machine to do development on your project.
>
> 2.  How many of the steps in your checklist can be automated using shell scripts or other small programs?
>
> 3.  How will newcomers know if they have completed the steps in the checklist correctly?
{: .challenge}

{% include links.md %}
