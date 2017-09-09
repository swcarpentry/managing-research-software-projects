---
title: "Compromise"
teaching: 20
exercises: 0
questions:
- "How can I improve my project's development processes without becoming overwhelmed?"
- "Under what circumstances can I suspend best practices?"
objectives:
- "Describe the concept of technical debt."
- "Discuss strategies for principled compromises in software development best practices."
keypoints:
- "Technical debt must often be accrued to get a project off the ground, but must eventually be paid down for a project to grow."
- "Use rapid iterative development to bring a project up to a minimally viable standard."
- "Software engineering best practices are not a goal unto themselves, but means to an end."
- "Ensure the scientific core of your project is sound. Otherwise, fix bugs when they come along, and then get back to science."
---

*   "Technical debt"
    *   Dissonance between (constantly refining) conceptual model and the model reflected in code
    *   Informed, deliberate suspension of best practices
    *   Term popularized by tech startup culture
*   Constant tradeoff
    *   Usually necessary to get a project off the ground
    *   Complicates sustained development
        *   Maintaining and extending requires going back and cleaning up
        *   Debt must be "paid down"...usually with interest!
*   None of the best practices discussed in this workshop are a goal unto themselves!
    *   They are means to an end
    *   What are the ends of your project?
        *   This will depend on whether the software is:
            *   One-time-use code supporting a single research project
            *   A generalized tool for analyzing particular types of data sets
            *   A software library supporting new analytical and methodological developments in a problem domain
        *   This will also depend on what part software plays in your career/research
            *   Is your job primarily to write software and/or support others in doing so?
            *   Is your job primarily to advance research in your field by producing new results, theories, models, methods, and data?
            *   Is your job primarily to teach, mentor, and/or manage others?
    *   Regardless, in science, priorities should be:
        *   Accuracy
        *   Performance
        *   ...
        *   ...
        *   ...
        *   User experience (we're not building dating apps here)
*   Rapid iterative development strategy
    *   Build a quick prototype
    *   Evaluate accuracy
    *   If performance is unsatisfactory
        *   Profile performance empirically
        *   Optimize code surgically
    *   Clean up code
*   Incremental improvement
    *   Don't try to FIX ALL TEH THINGS AT ONCE!
    *   Instead, whenever you touch a function to fix or extend it, clean it up then
        *   Check for code clarity
        *   Improve documentation and comments
        *   Write unit tests
    *   Improvements will accumulate quickly
*   Summary: compromise on best practices if you must
    *   But not on version control
    *   And not on automated testing
    *   Be deliberate
        *   Compromise is not an excuse to avoid learning or implementing best practices
        *   Just be mindful of whether they are helping you toward or distracting you from your highest priorities
*   Winning strategy: [stupidity-driven development][stupidity-driven]
    *   Write lots of tests for the scientific core of the code
    *   Dont fuss too much about everything else
    *   When a bug is encountered
        *   write a new regression test to reproduce the bug
        *   fix the bug
        *   get on with more important things
    *   Mantra: avoid wasting time writing tests for bugs that will never appear!

{% include links.md %}
