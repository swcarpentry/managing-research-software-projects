---
title: "Agile Development"
teaching: 15
exercises: 15
questions:
- "What is agile software development?"
- "What kinds of projects is agile development best suited to?"
objectives:
- FIXME
keypoints:
- FIXME
---

*  *Agile development* is a collection of techniques and practices that
    many people believe fit well with how researchers actually work, and
    that are a natural step up from what many good practitioners do when
    working solo.

*   The term "agile" was coined in 2001 to describe a "bottom-up" style of
    software project management based on short iterations and frequent
    feedback from both developers and customers.

*   Agile development practices are almost as old as programming, but they
    came into their own with the rise of the World Wide Web.
    *   The web made it possible to "release" software weekly, daily, or
        even hourly, since updating a server is a lot faster, and a lot less
        expensive, than shipping CDs to thousands of people.
    *   During the 1990s and early 2000s it seemed as if web programming
        tools were changing every single day.
        *   Multi-year development plans didn't make a lot of sense when everything
            they depended on would be obsolete by the time work started, much less
            by the time it finished.
    *   The growth of the web was aided by, and fuelled, the growth of
        the open source movement.
        *   People couldn't help noticing that most open source projects didn't have
            long-range plans, but nevertheless produced high-quality software faster
            than many closed-source commercial projects.

*   What is agile software development?
    *   Any methodology that relies on continuous or nearly continuous feedback.
    *   Agile methods break development down into short iterations, typically no
        more than two weeks long, and often as short as a single day.
    *   In each iteration, the team decides what to build next, designs it,
        builds it, tests it, and delivers it.
    *   As they're doing this, feedback loops at several scales help them get it
        right, and do it better next time.

*   The *iteration* is the primary feedback loop. Users often don't
    know what they want until they see it, so short cycles are a way to
    avoid spending too much time building what turns out to be the wrong
    thing.
    *   Most people can keep track of what they're doing for a few days
        at a time without elaborate Gantt charts, so short cycles allow them to
        spend proportionally less time coordinating with one another.
    *   Finding bugs becomes easier: instead of looking through weeks'
        or months' worth of software to find out where the problem is,
        developers usually only have to look at what's been written in the last
        few days.

![The Iteration Loop]({{ site.github.url }}/fig/iteration.png)

*   This "exploratory" approach is why many people think that agile is a
    good way to develop small-scale research software.
    *   Many researchers are their own users,
        and often can't know what they should write next until
        they've seen the output of the current program.

*   So what does agile development look like in practice?
    *   Easiest to understand in terms of other (nested) feedback loops.

*   A typical working day starts with a *stand-up meeting* where everyone in
    the team reports what they did the day before, what they're planning to
    do that day, and what's blocking them (if anything).
    *   It's called a "stand-up" meeting because it's usually held standing up,
        which encourages people to stay focused.
    *   Typical report:
        *   Yesterday:
            *   Fixed the bug that was making the mesh file reader
                crash on grid that are only one layer deep.
            *   Added code to the visualizer to render single-layer meshes.
        *   Today:
            *   Disable gradient shading for single-layer meshes.
            *   Add examples of single-layer meshes to documentaiton.
        *   Blockers:
            *   Don't understand how to make examples searchable by keyword.

*   Stand-up meetings are another agile feedback loop. Each day, the team
    gets feedback on the progress they're making, whether they're still on
    track to meet the iteration's goals, whether the technical decisions
    they're making are paying off, and so on:

![The Standup Meeting Loop]({{ site.github.url }}/fig/standup.png)

*   The key to making this work is that each task is at most a day long.
    *   Anything longer is broken into sub-tasks so that there's something
        substantial to report at every meeting.
    *   Without this rule, it's all too easy for someone to say, "Still working
        on X," several days in a row, which means that feedback, and the
        possibility of early course correction, are lost.

*   Once the stand-up meeting is over, everyone gets back to work.
    *   In many agile teams, this means sitting with a partner and doing *pair
        programming*:

![The Pair Programming Loop]({{ site.github.url }}/fig/pair.png)

*   The "driver", does the typing, while the "navigator" watches and
    comments.
    *   Every hour or so, the pair switches roles.

*   Pair programming is beneficial for several reasons:
    *   The navigator will often notice mistakes in the driver's
        code, or remember design decisions that the driver is too busy
        typing to recall.  This is the tightest of the feedback loops that
        make agile work, since feedback is nearly continuous.
    *   Pair programming spreads knowledge around: every piece of
        code has been seen by at least two people, which reduces the risk
        of "But I didn't know" mistakes.
    *   It also helps people pick up new skills: if you have just
        seen someone do something with two clicks, you will probably do it
        that way when it's your turn to drive, rather than spending two
        minutes doing it the way you always have.
    *   And most people are less likely to check Facebook every five
        minutes if someone else is working with them…

*   Many agile projects also use *test-driven development* (TDD).
    1.  Write a handful of tests that don't even run because the code they
        are supposed to test doesn't exist yet.
    2.  Write just enough code to make those tests pass.
    3.  Clean up what's just been written.
    4.  Commit it to version control.

![The TDD Loop]({{ site.github.url }}/fig/tdd.png)

*   TDD's advocates claim that:
    *   Writing tests first focuses people's minds on
        what their code is supposed to before they're psychologically biased in
        favor of it being supposed to do whatever they've just written actually
        does.
    *   Writing tests first ensures that code actually *is* testable: all too often, if
        someone spends a day writing software, they'll only discover at the end
        that there's no easy way to set up tests cases, run them, or check the
        results.

*   Evidence backing these claims is contradictory
    *   Many people advocate it strongly based on personal experience
    *   But most empirical studies haven't found a measurable benefit
    *   So maybe we're measuring the wrong things…

*   Final practice is *continuous integration*
    *   Every few minutes, or every time someone commits code to the version
        control repository, an automated process checks out a clean copy of the
        code, builds it, runs all the tests, and posts the results somewhere,
        such as a web page.
    *   If any of the tests fail, the continuous integration system notifies
        people by sending out email, texting them, or making the red light in
        the coffee room start blinking.
        *   We're not kidding about the blinking light: the more obvious it is that
            something's broken, the faster people will fix it, and the less likely
            they are to shame themselves by breaking it again.

![The Continuous Integration Loop]({{ site.github.url }}/fig/ci.png)

*   Continuous integration is the reality check that ensures that the
    software is always in a runnable state, so that it's always ready to
    give to users.
    *   Like TDD, it encourages people to work in small steps, which in turn
        makes short iterations possible.

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
    *   Most developers don't like writing plans before they code, or
        documentation when they're done.  Coincidentally, agile doesn't
        require them to do much of either.  It's therefore all too common for
        developers to say "we're agile" when what they mean is "we're not
        going to bother doing anything we don't want to".
        *   In reality, agile requires *more* discipline, not less, just as
            improvising well requires even more musical talent than playing a score
            exactly.
    *   On the flip side, many people don't like making decisions. After two
        decades of schooling, they want to be told what the assignment is and
        exactly what they have to do to get an 'A', a 'B', or whatever grade
        they're shooting for.
        *   Many become quite defensive when told that figuring out what to do is
            now part of their job, but that's as essential to agile development as
            it is to scientific research.
