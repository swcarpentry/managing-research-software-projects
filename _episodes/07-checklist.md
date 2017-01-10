---
title: "Checklists"
teaching: 5
exercises: 10
questions:
- "How should I handle tasks that need to be done repeatedly, but computers can't do automatically?"
objectives:
- "Explain when to use checklists rather than a build manager."
keypoints:
- "Use checklists for tasks that have to be done repeatedly, but can't be done by a computer."
- "Have new contributors go through checklists to look for omissions and inaccuracies."
---

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
