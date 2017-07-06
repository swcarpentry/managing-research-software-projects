---
title: "Sturdy Development"
teaching: 5
exercises: 10
questions:
- "What other kind of development process could my project use?"
objectives:
- "Explain the key features of sturdy development."
- "Explain why sturdy development is a good fit for many mature research software projects."
keypoints:
- "Sturdy development is a software development process based on planning suitable for larger teams and more mature projects."
- "Key features are division of labor, effort estimation, and long-term scheduling."
- "Sturdy development is most suitable for large projects with well-defined goals."
---

*   *Sturdy development* is a made-up term to describe "classic" software engineering practices
    *   Didn't need a name until agile came along
*   Best suited for situations in which:
    *   Stakeholders insist that developers make commitments to long-term goals (typical of grant cycles)
    *   Work is so large that division of labor is essential
*   Key assumption: measure twice, cut once
    *   The later a problem is caught, the more expensive it is to fix
    *   So careful up-front planning can pay for itself by reducing effort downstream
    *   Truest when the problem domain, good solution strategies, and technologies are all well understood

![Sturdy Lifecycle]({{"/fig/sturdy.png" | absolute_url}})

1.  *Gather requirements*: figure out what the software is supposed to do
    *   The responsibiliyt of the *product manager*
    *   While developers are working on version 4, she talks to stakeholders about what they want in version 5
    *   Never ask them what features they want in the software, but rather:
        *   What does it do now that you don't like?
        *   What can't you do that you'd like to be able to?
    *   Product manager collates these needs and figures out how the software should be changed to satisfy them
2.  *Analysis and estimation</em>: figure out how long features will take to implement
    *   Each team member is responsible for analyzing and estimating one or more features
    *   Must come up with a plausible rough design, and estimate how long it will take to implement
    *   Where possible, come up with two such plans:
        *   One for the whole feature
        *   One for a useful subset requiring less effort
    *   A&E presupposes an overall architecture for the system has already been defined
        *   Doesn't make sense to say, "We'll create a plugin to handle that" unless there's a plugin system
3.  *Prioritization*: because there's always more to do than there is time to do it
    *   Create a 3x3 grid whose axes are "effort" and "importance"
        *   Effort should be "an hour", "a day", "a week"
            *   Anything longer than a week should be broken into sub-tasks
        *   Importance is "low", "medium", "high"
    *   Each feature goes into one square
    *   Then draw a diagonal and throw away everything below it that requires a lot of effort but isn't important

![Prioritization]({{"/fig/prioritize.png" | absolute_url}})

4.  *Create a schedule*
    *   Who is going to do what, when?
    *   Do *not* shave estimates to make things fit
        *   Undermines trust on both sides and leads to "science fiction scheduling"
    *   Schedule is owned by the *project manager*, whose job it is to decide when to abandon or reschedule work and what to do instead
    *   E.g., if a high priority item is taking longer than expected, should it be put on hold and work started on something with lower priority requiring less effort?
    *   The earlier you let stakeholders know that things are going to be late (or aren't going to get done at all), the less unhappy they'll be
    *   Note: estimation improves with practice
5.  *Do the work*
    *   In practice, some work starts during A&E, since people need to prototype to see if their designs are plausible
    *   Testing and documentation start at the same time as coding
        *   Or even earlier: A&E should include estimates for time required to test and explain
    *   Also start deploying at the same time as development
        *   Needed for testing
        *   And need to test packaging and deployment along with everything else
6.  *Stop adding features* about 2/3 of the way through the allotted time
    *   Experience shows that teams need at least 1/3 of the overall cycle to fix bugs and tidy up

*   Sturdy development relies on having good requirements
    *   As unambiguous as a legal contract or a theorem proof
    *   I.e., two well-informed practitioners should reach the same conclusions about correctness
*   "The system will reformat data files as they are submitted" isn't enough---should have:
    *   Only users who have logged in by providing a valid user name and password can upload files.
    *   The system allows users to upload files via a secure web form.
    *   The system accepts files up to 16MB long.
    *   The system accepts files in PDB and RJCS-1 format.
    *   The system converts files to RJCS-2 format before storing them.
    *   The system displays an error message page if an uploaded file cannot be parsed, but takes no other action.
    *   Etc.
*   Best to [specify requirements as tests]({{"/11-testing/" | absolute_url}}), but those can still require human-readable explanation

> ## Prioritize
>
> 1.  Draw a 3x3 grid of the kind described above.
> 2.  Pick 3-4 open issues for your current project.
> 3.  Decide where each one belongs on the grid.
>     Are any of them so large that they should be broken down into sub-tasks?
{: .challenge}

> ## Write Requirements
>
> 1.  Write an unambiguous specification of a feature you would like to add to your current project.
> 2.  Swap specifications with your partner.
> 3.  What is the least helpful (or most damaging) implementation of your partner's feature you can think of
>     that would technically satisfy the specification they wrote?
{: .challenge}
