---
layout: page
title: "Lesson Design"
permalink: /design/
---

## Contents
{:.no_toc}

* Jekyll will replace this line with an auto-generated table of contents.
{:toc}

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

## Stage 1: Assumptions

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
    *   One full day 09:00-16:00
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

## Stage 2: Desired Results

### Questions

How do I...

*   ...know what state my project is in?
*   ...figure out what the team ought to work on next?
*   ...figure out when they'll be done (and what "done" means)?
*   ...adjust plans when things go wrong?
*   ...make it easy for other people to contribute?
*   ...manage contributions from other developers?
*   ...create an installable, usable version of my project?
*   ...pass these skills on to my team?

### Skills

I can...

1.  ...report my status clearly and succinctly in a stand-up meeting.
2.  ...give others feedback on the content and presentation of their stand-up reports.
3.  ...critique and improve bug reports and status reports.
4.  ...create a development schedule for a project
    given a set of tasks with priorities and time estimates.
5.  ...(re-)organize the files in a small to medium-sized software project
    according to [Noble's Rules][noble-rules]
6.  ...implement continuous integration by connecting
    a regression test script to a GitHub repository using Travis-CI.
7.  ...apply [Taschuk's Rules][taschuk-rules] to make software more robust.
8.  ...create an installable Python package.

### Concepts

I know...

*   ...that participating in a software project is a separate skill from programming.
*   ...what the core practices of agile and sturdy development are
    and what kinds of projects each is best suited for.
*   ...that managing a software project depends on planning and feedback at multiple timescales.
*   ...that simple off-the-shelf tools can make participation in software projects easier.

### Tools

I can use...

*   ...[GitHub][github] for project management (issues and pull requests).
*   ...[Make][make-lesson] for task automation.
*   ...[Travis-CI][travis-ci] for continuous integration.
*   ...[Sphinx][sphinx] for documentation generation.
*   ...[Pip and Setuptools][python-packaging] to create and install packages.
*   ...[Waffle][waffle] for backlog management.

## Stage 3: Learning Plan

### Summative Assessment

*   Mid-day: learners will set up continuous integration for a small project
*   End of day: learners will develop a one-minute pitch for their real project

### Agile Development (09:00)

*   Teaching: 20 min
*   Exercises: 40 min
    *   Do standup reports and critique others' standup reports
        *   Groups of three with cellphone recording
    *   Test-driven development
        *   Turn prose description into tests
        *   Turn tests into functions
        *   All done with pair programming

### Project Organization (10:00)

*   Teaching: 15 min
*   Exercises: 15 min
    *   Reorganize code according to Noble's Rules

### Coffee (10:30): 15 min

### Robustifying Code (10:45)

*   Teaching: 15 min
*   Exercises: 15 min
    *   Identify violations of Taschuk's Rules

### Continuous Integration (11:15)

*   Teaching: 15 min
*   Exercises: 15 min
    *   Set up Travis-CI and a GitHub repository
    *   Automatically regenerate documentation using Sphinx
    *   Note: part of the exercise will be done during the teaching time by following along

### Morning Review (11:45): 15 min

### Lunch (12:00): 60 min

*   Think about one technique or tool you like and how to pitch it

### Sturdy Development (13:00)

*   Teaching: 30 min
*   Exercises: 30 min
    *   Critique a couple of badly-written issues in a repo
    *   Write short workflow description in three-part notation (actor-view-model)

### Packaging and Dependency Management (14:00)

*   Teaching: 15 min
*   Exercises: 30 min
    *   Capture project dependencies in requirements.txt
    *   Create installable Python package

### Coffee (14:45): 15 min

### Staying on Track

*   Teaching: 15 min
    *   Barriers to participation
    *   Code of conduct
    *   Developing a mission statement
*   Exercises: 30 min
    *   Create and deliver a mission statement (1-minute pitches)

### Wrap-Up (15:45)

*   Discussion: 15 min

{% include links.md %}
