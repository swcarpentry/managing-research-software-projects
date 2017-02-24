---
title: "Agile Development"
teaching: 5
exercises: 10
questions:
- "What kind of development process should my project use?"
objectives:
- "Explain the key features of agile development."
- "Explain why agile development is a good fit for many new research software projects."
keypoints:
- "Agile development is a software development process based on short iterations and rapid feedback."
- "Key feedback loops are pair programming, test-driven development, continuous integration, and stand-up meetings."
- "Agile works well for exploratory projects."
- "Agile depends on high-bandwidth communication between developers and users, and on developers wanting to be empowered."
---

*   *Agile development* fits well with how most researchers work
*   Term coined in 2001 to describe bottom-up style of software project management
    based on short iterations and frequent feedback at many scales
    *   Practices are almost as old as programming,
        but came into their own with the rise of the web
    *   Made daily (even hourly) "releases" possible
    *   Multi-year development plans didn't make sense when everything
        they depended on would be obsolete by the time work started

![Agile Feedback Loops]({{"/fig/agile-feedback.png" | absolute_url}})

*   Key feature is *short iterations*: single day to two weeks
    *   In each iteration, the team decides what to build next, designs it,
        builds it, tests it, and delivers it
    *   Users don't  know what they want until they see it,
        so short cycles avoid building things people don't actually want
    *   Most people can organize time for a few days without much effort,
        so short cycles reduce proportion of time spent on coordination
*   This exploratory approach makes agile a good fit for young research software
    *   Researchers often can't know what to write next
        until they've seen the output of the current program
*   Every day starts with a *stand-up meeting* where everyone reports:
    *   What they did the day before
    *   What they're planning to do that day
    *   What's blocking them (if anything)
    *   Called a "stand-up" meeting because it's held standing up,
        which encourages people to stay focused
    *   Encourages people to break work down into tasks that are at most one day long
    *   If someone to says "still working on X" several days in a row,
        they're not giving meaningful feedback on their progress
*   The PI is typically the *product owner* with ultimate say over what functionality the software has
    *   Not necessarily the same as what changes are made, since one feature can satisfy many needs (and one need may require many new features)
*   Agile development works best when:
    1.  Requirements are constantly changing, i.e., long-range planning
        isn't possible anyway. This is often the case for scientific
        research, particularly at the small scale.
    2.  Developers and users can communicate continuously, or at worst
        daily or weekly. Again, this is normal for small-scale research,
        where developers and users are the same people.
    3.  The team is small, so that everyone can take part in a single
        stand-up meeting. This is usually also true, though getting
        everyone to show up for a morning meeting is a challenge in many
        labs.
    4.  Team members are disciplined enough not to use "agile" as an
        excuse for cowboy coding.
    5.  They actually *like* being empowered.
*   The last two points are the most important.
    *   Most developers don't like writing plans before they code, or documentation when they're done.
        *   Coincidentally, agile doesn't require them to do much of either.
        *   It's therefore all too common for developers to say "we're agile"
            when what they mean is "we're not going to bother doing anything we don't want to".
        *   In reality, agile requires *more* discipline, not less, just as
            improvising well requires even more musical talent than playing a score
            exactly.
    *   In addition, some people don't like making decisions
        *   Many become quite defensive when told that figuring out what to do is
            now part of their job, but that's as essential to agile development as
            it is to scientific research.

> ## Are You Agile?
>
> 1.  Which of the key agile practices described above are you currently using?
> 2.  Which do you think you and your team would actually adopt in the next 3-6 months?
> 3.  Which do you think are not good fits to your needs or situation?
{: .challenge}

{% include links.md %}
