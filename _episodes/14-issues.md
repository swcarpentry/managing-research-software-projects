---
title: "Issues"
teaching: 5
exercises: 10
questions:
- "How can I keep track of what needs to be done?"
objectives:
- "Describe what sorts of things should be recorded in an issue-tracking system."
- "Describe what goes into a well-written issue."
- "Explain how issue-tracking systems can be used to implement workflows."
- "Explain how issue-tracking systems can be used to focus attention where it's needed."
keypoints:
- "An issue-tracking system is a shared to-do list for a project."
- "Every issue has a few mandatory fields to help with searching, and free-form text for details."
- "Every issue is in a particular state."
- "A project can define a workflow by specifying who can change tickets' states when."
- "Use tickets to prioritize work: what needs be done now, what can be deferred until later."
---

*   Issue-tracking tools are often called bug trackers
    *   Well-organized teams use them as a shared to-do list to manage everything
    *   "Version control tells us where we've been; issue tracking tells us where we're going."
*   Every task is recorded as a separate ticket
    *   Unique ID
    *   One-line summary to aid browsing
    *   Status
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

![Issue Lifecyce]({{ site.github.url }}/fig/issue-lifecycle.png)

*   Don't worry about any of this until people are actually filing issues
*   Key use: prioritization
    1.  What has to be done right now?
    2.  What should be done soon?
    3.  What can safely be left until later?
*   Criteria for decision:
    1.  How much do we need this?
    2.  How long will it take?

![Prioritization]({{ site.github.url }}/fig/prioritize.png)

> ## What's On Your List?
>
> 1.  What are the top 10 items on your project's to-do list?
> 2.  How sure are you that your collaborators and users would agree with your selection?
{: .challenge}

> ## What's Missing?
>
> Look at the issue lifecycle diagram above.
> What steps or transitions would you add?
> Which ones would you remove?
> Which ones would you make other people responsible for?
{: .challenge}

> ## What's Your Lifecycle?
>
> 1.  What states can your project's issues be in?
> 2.  What state transitions are allowed?  ("Any to any" is a common and acceptable answer.)
> 3.  Who decides when an issue can move from one state to another?
{: .challenge}

{% include links.md %}
