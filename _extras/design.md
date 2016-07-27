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
    *   Must be familiar with:
        *   [the Unix shell][shell-lesson]
        *   [Make][make-lesson]
        *   [version control][git-lesson] (enough to follow pull/edit/commit/push/PR instructions)
        *   [Python][python-lesson] (because we have to use some programming language for examples)
*   Data
    *   Start with a copy of a badly-organized software project
    *   Improve it in pieces throughout the course

## Stage 1 - Desired Results

### Essential Questions

How do I...

*   ...know what state my project is in?
*   ...figure out what the team ought to work on next?
*   ...figure out when they'll be done (and what "done" means)?
*   ...adjust plans when things go wrong?
*   ...manage contributions from other developers?
*   ...create an installable, usable version of my project?

### Concepts

Learners will know that...

*   ...participating in a software project is a learnable skill
*   ...managing a software project depends on making plans and having feedback at several scales
*   ...off-the-shelf tools can provide part of the information needed to manage a project

### Summative Assessment

*   Midpoint: triage a set of issues in a GitHub repository
    and create a work plan for the upcoming release.
*   Final: create an installable version of a small project.

### Skills

Learners can:

1.  ...explain the core practices of agile and sturdy development
    and identify the kinds of projects each is best suited for.
2.  ...report their status clearly and succinctly in a stand-up meeting.
3.  ...give others feedback on their stand-up reports (content and presentation).
4.  ...critique and improve bug reports and status reports.
5.  ...create a development schedule for a project
    given a set of tasks with priorities and time estimates.
6.  ...implement regression tests driven by
    a single script with an appropriate exit status
7.  ...implement continuous integration by connecting a GitHub repository
    to [Travis-CI][travis-pr].
8.  ...automatically generate documentation for a project
    from information embedded in the project's source code.
9.  ...package a release.

[git-lesson]: https://swcarpentry.github.io/git-novice/
[make-lesson]: https://swcarpentry.github.io/make-novice/
[python-lesson]: https://swcarpentry.github.io/python-novice-gapminder/
[rse]: http://www.rse.ac.uk/
[shell-lesson]: https://swcarpentry.github.io/shell-novice/
[travis-pr]: https://docs.travis-ci.com/user/pull-requests
