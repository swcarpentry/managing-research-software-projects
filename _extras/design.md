---
layout: page
title: "Lesson Design"
permalink: /design/
---
## Process Used

This lesson was developed using a slimmed-down variant of the "Understanding by Design" process.
The main sections are:

1.  Assumptions about audience, time, etc.

2.  Desired results:
    overall goals, summative assessments at half-day granularity, what learners will be able to do, what learners will know.

3.  Learning plan:
    each episode has a heading that summarizes what will be covered,
    then estimates time that will be spent on teaching and on exercises,
    while the exercises are given as bullet points.

While this looks like a waterfall process, in practice we did this:

1.  Draft the assumptions.

2.  Do one bullet point for each of several learning milestones.

3.  Draft the desired results.

4.  Update the learning milestones (still as just one bullet point each, no time estimates or exercises).

5.  Get early feedback from four people.

6.  Do a full pass to flesh out the assumptions and add time estimates and exercises.

7.  Ask for feedback and start iterating (mostly to cut things).

## Stage 0 - Assumptions

*   Audience
    *   [Research software engineers][rse]
        who are now responsible for a small to medium-sized software project (defined below)
    *   Program frequently, use version control, know what unit testing is (but may not actually have written many tests)
    *   No previous exposure to project management or software project management tools
*   Constraints
    *   One full day 09:00-17:00
        *   06:30 teaching time
        *   1:00 for lunch
        *   0:30 total for two coffee breaks
    *   Learners use native installs on their own machines
        *   Must be familiar with the Unix shell
        *   Know enough version control to follow along/imitate a pull/edit/commit/push/PR cycle
*   Data
    *   Start with a copy of a badly-organized software project
    *   Improve it in pieces throughout the course
*   Focus on practices common to all real-world development methodologies
    *   Automated builds (mini-lesson on Make)
    *   Regression testing
    *   Continuous integration

## Stage 1 - Desired Results

### Goals

Learners can:

1.  ...explain the core practices of agile and sturdy development
    and identify the kinds of projects each is best suited for.
2.  ...implement continuous integration.
3.  ...automate basic management tasks using a self-documenting Makefile.
4.  ...automatically generate documentation for a project
    from information embedded in the project's source code.
5.  ...coach other developers on pair programming.
6.  ...report their own status clearly and succinctly in a stand-up meeting.
7.  ...coach other developers on reporting status in stand-up meetings.
8.  ...critique and improve bug reports and status reports.
9.  ...create a development schedule for a project
    given a set of tasks with priorities and time estimates.
10. ...create a release.

### Summative Assessment

*   Midpoint: triage a set of issues in a GitHub repository
    and create a work plan for the upcoming release.
*   Final: create an installable version of a small project.

### Essential Questions

How do I...

*   ...know what state my project is in?
*   ...figure out what the team ought to work on next?
*   ...figure out when they'll be done (and what "done" means)?
*   ...adjust plans when things go wrong?
*   ...create an installable, discoverable version of my project?

### Concepts

Learners will know that...

*   FIXME

[rse]: http://www.rse.ac.uk/
