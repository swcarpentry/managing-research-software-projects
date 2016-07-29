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
    *   Overall goals
    *   Summative assessments at half-day granularity
    *   What learners will be able to do, what they will know, etc.

3.  Learning plan
    *   TBD
    *   See [this lesson][gapminder-learning-plan] for an example

## Stage 0 - Assumptions

*   Audience
    *   [Research software engineers][rse]
        who are now responsible for a small to medium-sized software project (defined below)
    *   Program frequently, use version control, know what unit testing is (but may not actually have written many tests)
    *   No previous exposure to project management or software project management tools
*   Projects
    *   6×6: half a dozen people working for about six months
    *   Both numbers may vary up and down, but:
        *   Group is small enough to have lunch together (i.e., a single cohesive unit)
        *   Timescale is short enough that personnel turnover probably isn't an issue
*   Constraints
    *   One full day 09:00-17:00
        *   1:00 for lunch
        *   0:30 total for two coffee breaks
        *   So 6:30 teaching time
    *   Learners use native installs on their own machines plus web resources (e.g., GitHub)
    *   Must be familiar with:
        *   [the Unix shell][shell-lesson]
        *   [Make][make-lesson]
        *   [Git][git-lesson] (enough to follow pull/edit/commit/push/PR instructions and use GitHub)
        *   [Python][python-lesson] (because we have to use some programming language for examples)
*   Running Example
    *   Start with a badly-organized software project
    *   Improve it in pieces throughout the course
*   Resources
    *   [Noble's Rules](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1000424)

## Stage 1 - Desired Results

### Essential Questions

How do I...

*   ...know what state my project is in?
*   ...figure out what the team ought to work on next?
*   ...figure out when they'll be done (and what "done" means)?
*   ...adjust plans when things go wrong?
*   ...make it easy for other people to contribute?
*   ...manage contributions from other developers?
*   ...create an installable, usable version of my project?

### Concepts

Learners will know that...

*   ...participating in a software project is a learnable skill
*   ...managing a software project depends on making plans and having feedback at several timescales
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
3.  ...give others feedback on the content and presentation of their stand-up reports.
4.  ...critique and improve bug reports and status reports.
5.  ...create a development schedule for a project
    given a set of tasks with priorities and time estimates.
6.  ...organize the files in a small to medium-sized software project
7.  ...implement regression tests driven by
    a single script with an appropriate exit status
8.  ...implement continuous integration by connecting
    a regression test script and a Git repository.
9.  ...create an installable Python package.

### Tools

Learners will use:

*   [GitHub][github] for project management (issues and pull requests)
*   [Make][make-lesson] for task automation
*   [Travis-CI][travis] for continuous integration
*   [Sphinx][sphinx] for documentation generation
*   [Pip and Setuptools][python-packaging] to create and install packages
*   [Waffle][waffle] for backlog management
*   Cellphones to record themselves giving status reports
*   Lots and lots of sticky notes

[gapminder-learning-plan]: http://swcarpentry.github.io/python-novice-gapminder/design/#stage-2---learning-plan
[git-lesson]: https://swcarpentry.github.io/git-novice/
[github]: https://github.com/
[make-lesson]: https://swcarpentry.github.io/make-novice/
[python-lesson]: https://swcarpentry.github.io/python-novice-gapminder/
[python-packaging]: https://packaging.python.org/
[rse]: http://www.rse.ac.uk/
[shell-lesson]: https://swcarpentry.github.io/shell-novice/
[sphinx]: http://www.sphinx-doc.org/
[travis-pr]: https://docs.travis-ci.com/user/pull-requests
[travis]: https://travis-ci.org/
[waffle]: http://waffle.io
