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
    *   Each episode has a heading that summarizes what will be covered,
        then estimates time that will be spent on teaching and on exercises.
    *   The exercises are outlined to make expectations concrete.

## Stage 1 - Assumptions

*   Audience
    *   [Research software engineers][rse]
        who are now responsible for a small to medium-sized software project (defined below)
    *   Program frequently, use version control, know what unit testing is (but may not actually have written many tests)
    *   No previous exposure to project management or software project management tools
*   Projects
    *   3×6: three people working for about six months
    *   Both numbers may vary up and down, but:
        *   Group is small enough to have lunch together (i.e., a single cohesive unit)
        *   Timescale is short enough that personnel turnover isn't an issue
    *   Some or all of the team members may be multi-tasking on other projects
    *   Building digital scientific instruments rather than doing exploratory data analysis
        *   E.g., creating a library, an application, or a pipeline
        *   May be starting from scratch
        *   But more likely cleaning up, rewriting, and integrating bits and pieces
    *   The principal scientific investigator (PI) *isn't* a member of the development team
*   Constraints
    *   One full day 09:00-17:00
        *   06:30 teaching time
        *   1:00 for lunch
        *   0:30 total for two coffee breaks
    *   This means we cannot introduce complex new tools
        *   But can add extensions to tools participants are already familiar with
    *   Attendees must be familiar with:
        *   [the Unix shell][shell-lesson]
        *   [Make][make-lesson]
        *   [Git][git-lesson] (enough to follow pull/edit/commit/push/PR instructions and use GitHub)
        *   [Python][python-lesson] (because we have to use some programming language for examples)
*   Running Example
    *   Start with a badly-organized software project
    *   Improve it in pieces throughout the course
*   Resources
    *   [Noble's Rules][noble-rules]
    *   [Jenkins' Project Primer][jenkins-primer]
    *   [Taschuk's Rules][taschuk-rules]

## Stage 2 - Desired Results

### Essential Questions

How do I...

*   ...know what state my project is in?
*   ...figure out what the team ought to work on next?
*   ...figure out when they'll be done (and what "done" means)?
*   ...adjust plans when things go wrong?
*   ...make it easy for other people to contribute?
*   ...manage contributions from other developers?
*   ...create an installable, usable version of my project?
*   ...pass these skills on to my team?

### Concepts

Learners will know that...

*   ...participating in a software project is a separate skill from programming.
*   ...managing a software project depends on planning and getting feedback at multiple timescales.
*   ...a few simple off-the-shelf tools can reduce or remove many barriers to participation.

### Summative Assessment

*   Learners will draw up a prioritized plan for work on their own projects
    *   Where "work" includes "educating stakeholders"

### Skills

Learners can:

1.  ...explain the core practices of agile and sturdy development
    and identify the kinds of projects each is best suited for.
2.  ...report their status clearly and succinctly in a stand-up meeting.
3.  ...give others feedback on the content and presentation of their stand-up reports.
4.  ...critique and improve bug reports and status reports.
5.  ...create a development schedule for a project
    given a set of tasks with priorities and time estimates.
6.  ...(re-)organize the files in a small to medium-sized software project
    according to [Noble's Rules][noble-rules]
7.  ...implement continuous integration by connecting
    a regression test script to a GitHub repository using Travis-CI.
9.  ...apply [Taschuk's Rules][taschuk-rules] to robustify software.
10. ...create an installable Python package.
11. ...pass their skills on to teammates.

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

## Stage 3 - Learning Plan

### Agile Development (09:00)

*   Teaching: 20 min
*   Exercises: 60 min
    *   Do standup reports and give feedback on others' standup reports
    *   Pair program and critique
    *   Test-driven development
        *   Turn prose description into tests
        *   Turn tests into function

### Coffee (10:20): 15 min

### Sturdy Development (10:35)

*   Teaching: 30 min
*   Exercises: 50 min
    *   Give feedback on a small set of issues filed in a repo
    *   Convert project backlog with time estimates into schedule
*   Note: will cover code review later when looking at Taschuk's Rules

### Morning Review (11:55): 10 min

### Lunch (12:05): 55 min

*   Think about one technique or tool you like and how to pitch it

### Project Organization (13:00)

*   Teaching: 15 min
*   Exercises: 15 min
    *   Reorganize code according to Noble's Rules

### Robustifying Code (13:30)

*   Teaching: 15 min
*   Exercises: 15 min
    *   Identify violations of Taschuk's Rules

### Continuous Integration (14:00)

*   Teaching: 15 min
*   Exercises: 15 min
    *   Set up Travis-CI and a GitHub repository
    *   Automatically regenerate documentation using Sphinx

### Coffee (14:30): 15 min

### Packaging and Dependency Management (14:45)

*   Teaching: 15 min
*   Exercises: 25 min
    *   Capture project dependencies in requirements.txt
    *   Create installable Python package

### Lightning Presentations (15:25)

*   Learners' 1-minute pitches of other techniques and tools: 20 min

### Wrap-Up (15:45)

*   Discussion: 15 min

[gapminder-learning-plan]: http://swcarpentry.github.io/python-novice-gapminder/design/#stage-2---learning-plan
[git-lesson]: https://swcarpentry.github.io/git-novice/
[github]: https://github.com/
[jenkins-primer]: http://www.nickjenkins.net/prose/projectPrimer.pdf
[make-lesson]: https://swcarpentry.github.io/make-novice/
[noble-rules]: http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1000424
[python-lesson]: https://swcarpentry.github.io/python-novice-gapminder/
[python-packaging]: https://packaging.python.org/
[rse]: http://www.rse.ac.uk/
[shell-lesson]: https://swcarpentry.github.io/shell-novice/
[sphinx]: http://www.sphinx-doc.org/
[taschuk-rules]: https://github.com/oicr-gsi/robust-paper
[travis-pr]: https://docs.travis-ci.com/user/pull-requests
[travis]: https://travis-ci.org/
[waffle]: http://waffle.io
