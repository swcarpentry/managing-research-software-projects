---
title: "Basics"
teaching: 15
exercises: 10
questions:
- "How should I manage work using version control?"
- "How should I handle tasks I do repeatedly?"
- "How should I handle tasks that need to be done repeatedly, but computers can't do automatically?"
- "How can I keep track of what needs to be done?"
objectives:
- "Explain how to use feature branches to manage software development."
- "Explain what build managers were originally designed to do, and what else they are now used to do."
- "Make a build file self-explaining."
- "Explain when to use checklists rather than a build manager."
- "Describe what sorts of things should be recorded in an issue-tracking system."
- "Describe what goes into a well-written issue."
- "Explain how issue-tracking systems can be used to implement workflows."
- "Explain how issue-tracking systems can be used to focus attention where it's needed."
keypoints:
- "Use version control for everything created manually, not just code."
- "Create a new branch for each feature."
- "Only use that branch for that feature."
- "Merge and delete the branch when the feature is complete."
- "Use a build manager to manage repetitive tasks."
- "Make build files explain themselves."
- "Use checklists for tasks that have to be done repeatedly, but can't be done by a computer."
- "Have new contributors go through checklists to look for omissions and inaccuracies."
- "An issue-tracking system is a shared to-do list for a project."
- "Every issue has a few mandatory fields to help with searching, and free-form text for details."
- "Every issue is in a particular state."
- "A project can define a workflow by specifying who can change tickets' states when."
- "Use tickets to prioritize work: what needs be done now, what can be deferred until later."
---

## DRY: Don't Repeat Yourself

*   Usually applied to nouns (code)
*   Just as true for verbs (actions)
*   The only thing you can accomplish by typing something repeatedly is to get it wrong

## Version Control

*   We assume your project is already under version control
    *   If not, this may not be the right course for you
*   We also assume you use version control for everything created by human beings
    *   A major reason for the existence and survival of tools like LaTeX and Markdown
    *   Collaboration would be a *lot* easier if version control systems knew
        how to manage rich document formats...
*   Use a *[feature branch workflow]({{"/reference/#feature-branch" | absolute_url}})*
    *   Designate one branch as the main development branch (typically called `master`)
    *   Create a new branch for each feature from `master`
    *   Only use that branch for that feature
    *   Merge the branch when the feature is done

## Build Manager

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

## Checklists

*   A checklist is a build file meant to be executed by human beings
    *   *[The Checklist Manifesto][gawande-checklist-manifesto]*
        describes how use of checklists cuts fatalities in surgery significantly,
        along with many other examples
*   Use them for anything that *can't* be done automatically by a machine
*   Keep in version control
    *   Ask every new contributor/user to use *and give feedback*
*   Include a contact email address in every checklist

## Issue Tracking

*   Issue-tracking tools are often called bug trackers
    *   Well-organized teams use them as a shared to-do list to manage everything
    *   "Version control tells us where we've been; issue tracking tells us where we're going."
*   Every task is recorded as a separate ticket
    *   Unique ID
    *   One-line summary to aid browsing
    *   Status (sometimes organized by [stages of grief][twitter-grief])
    *   Owner (i.e., who's responsible)
    *   Full description that may include screenshots, error messages, etc.
    *   History: who created it when, how it has been modified
    *   Threaded discussion

~~~
ID: 1278
Created-By: mummy
Owned-By: wolfman
State: assigned
Summary: Message file reader crashes on accented characters
Description:
1.  Create a text file called 'accent.msg' containing the message
    "Pümpernickel" (with an umlaut over the 'u').

2.  Run 'python mindcontrol.py --all --message accent.msg'

Program crashes with the message "No encoding for [] on line 1 of 'accent.msg'".
([] shows where a solid black box appears in the output instead of a printable
character.)
~~~
{: .source}

*   More sophisticated systems allow people to:
    *   Record dependencies between tickets
    *   Estimate how long work will take
    *   Record how long work actually took
*   Can be used to make the development lifecycle explicit
    *   I.e., only allow certain state transitions
    *   And notify interested parties of state transitions

![Issue Lifecycle]({{"/fig/issue-lifecycle.png" | absolute_url}})

*   Don't worry about any of this until people are actually filing issues
*   Key use: prioritization
    1.  What has to be done right now?
    2.  What should be done soon?
    3.  What can safely be left until later?
*   Another use is to show that you're working on someone
    *   Assigning to someone or setting an "in progress" tag can save a lot of wasted effort
    *   And reassure anxious users
*   Criteria for decision:
    1.  How much do we need this?
    2.  How long will it take?

> ## How Do You Manage Your Repository?
>
> Describe in 3-4 bullet points how you actually manage your version control repository.
> How often are you working on several things simultaneously?
{: .challenge}

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

> ## What's On Your List?
>
> 1.  What are the top 3 items on your project's to-do list?
> 2.  How sure are you that your collaborators and users would agree with your selection?
{: .challenge}

> ## What's Your Lifecycle?
>
> 1.  What states can your project's issues be in?
> 2.  What state transitions are allowed?  ("Any to any" is a common and acceptable answer.)
> 3.  Who decides when an issue can move from one state to another?
{: .challenge}

{% include links.md %}
