---
title: "Introduction"
teaching: 5
exercises: 10
questions:
- "What is the scope of this class?"
- "What does 'done' look like?"
objectives:
- FIXME
keypoints:
- FIXME
---

*   [What is a research software engineer](http://www.rse.ac.uk/who.html) (RSE)?
    *   Combine expertise in programming with an in-depth understanding of research
    *   Typically have:
        *   An advanced degree in a research discipline
        *   Lots of experience developing software (often acquired while working on their thesis)...
        *   ...but little or no formal training in software engineering
    *   "The astronomers who build telescopes so that others can study stars"
*   What *isn't* an RSE?
    *   Sys admin (although many RSEs wind up doing a lot of systems administration)
    *   Lab tech (although sometimes classified as such)
    *   Principal investigator (although RSEs occasionally become PIs on infrastructure projects)
*   What do RSEs do?
    *   *Design, write, test, and maintain software*
    *   Manage data (or build tools to fetch, filter, organize, and process data)
    *   Deploy and run software (overlaps with sys admins)
*   Are you an RSE?
    1.  Are you employed to develop software for research?
    1.  Are you spending more time developing software than conducting research?
    1.  Are you employed as a postdoctoral researcher,
        even though you predominantly work on software development?
    1.  Are you the person who does computers in your research group?
    1.  Are you sometimes not named on research papers
        despite playing a fundamental part in developing the software used to create them?
    1.  Do you lack the metrics needed to progress your academic career,
        like papers and conference presentations,
        despite having made a significant contribution through software?
*   Key differences between research software and "normal" projects
    *   Requirements may be either:
        *   Discovered as we go along (exploring)
        *   Relatively stable (engineering)
    *   Problem is *subtle* as well as *complicated*
        *   Control flow may be very simple...
        *   ...but figuring out exactly what coefficients and indexes to use can be very hard
*   For our purposes:
    *   3x3: three people for three months
    *   Contributors are frequently time-slicing other projects
    *   "Everybody makes coffee"
*   What does "done" look like?
    *   Software can be used by people other than original authors
        *   Reproducibility meaningless without this
    *   Reasonably confident that results are correct
        *   As trustworthy as physical experiment
    *   Small changes and extensions are easy
        *   I.e., researchers can safely make small changes to code
    *   Fast enough to be useful
*   What do RSEs need to know?
    *   Programming language(s) - in more depth than most of their research colleagues
    *   Version control - ditto
    *   Build and test tools - often the only one on their team doing any of this
    *   Performance analysis and tuning - ditto
    *   Software lifecycle management - often de facto process owners
        *   What needs to be done?
        *   Why?
        *   Who's doing it?
        *   When is it due?
        *   What state is it in (i.e., are we done yet)?
        *   Where is everything?
        *   How do we do things?
*   Outline of this class
    *   Software lifecycles for small research projects
    *   How to implement simple lifecycles with off-the-shelf tools
*   What's not included
    *   Software architecture - see [AOSA](http://aosabook.org) for ideas
    *   Refactoring - see [Feathers](https://www.amazon.com/Working-Effectively-Legacy-Michael-Feathers/dp/0131177052/)
    *   ...and much else
