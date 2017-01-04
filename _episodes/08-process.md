---
title: "Step 6: Choose a Process"
teaching: 5
exercises: 10
questions:
- "What is agile software development?"
- "What is sturdy software development?"
- "What kind of development process should my project use?"
objectives:
- "FIXME"
keypoints:
- "FIXME"
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


Hello, and welcome to the fourth episode of the Software Carpentry
lecture on software engineering. In this episode, we'll look at a
software development methodology that many people feel is well suited to
large, complex projects.

Before the term "agile" was invented in 2001, this approach didn't have
a name: it was just how big software engineering projects were run.
Today, it's sometimes called "traditional" software engineering; fans of
agile often call it "big design up front" (BDUF) or something less kind.

We prefer the label "sturdy" because it puts a more positive spin on
things. While agile is all about reacting quickly and taking advantage
of opportunities as they arise, sturdy is about carrying the load of
large projects—it emphasizes predictability..

Let's start by looking at what sturdy development *isn't*. A *waterfall
model* of software development divides the process into distinct stages;
information flows from one stage to the next like water falling down a
hill.

Even in 1970, when this model was first given a name, people knew it
didn't work. Nobody has 20/20 foresight; requirements are always
discovered or changed as software is designed, while designs are re-done
based on what's learned during implementation, implementations are
modified as testing finds problems, and so on.

But that doesn't mean that up-front planning and design are pointless.
Thirty-five years ago, Barry Boehm and others discovered that the later
a bug is found, the more expensive fixing it is. What's more, the cost
curve is exponential: as we move from requirements to design to
implementation to testing to deployment, the cost of fixing a problem
increases by a factor of 3 to 10 at each stage, and those increases
multiply:

![The Cost of Fixing Problems]({{ site.github.url }}/fig/costs.png)

The obvious implication is that time invested in up-front design can pay
off many-fold if it prevents mistakes being made in the first place. It
isn't always possible to do—people may not know what they want until
they see something running, or tools may change so quickly that anything
we design today will be obsolete by the time it's implemented—but very
few programmers have ever said, "I wish I'd spent *less* time thinking
about this before I started coding."

Here's what a sturdy development lifecycle might look like in practice:

![Sturdy Software Development Lifecycle]({{ site.github.url }}/fig/lifecycle.png)

The first step is to gather requirements, i.e., to figure out what the
software is supposed to do. This is the *product manager*'s job; while
the developers are working on version 4, she talks to the customers
about what they want version 5 to do.

Crucially, she should never ask them what features they want in the
software; that's up to her to figure out. Instead, she should ask, "What
does it do now that you don't like?" and, "What can't you do that you'd
like to be able to?" She collates these needs and figures out how the
software should be changed to satisfy them.

Good requirements are as unambiguous as a legal contract. "The system
will reformat data files as they are submitted" isn't enough guidance;
instead, the requirements should read:

1.  Only users who have logged in by providing a valid user name and
    password can upload files.

2.  The system allows users to upload files via a secure web form.

3.  The system accepts files up to 16MB long.

4.  The system accepts files in PDB and RJCS-1 format.

5.  The system converts files to RJCS-2 format before storing them.

6.  The system displays an error message page if an uploaded file cannot
    be parsed, but takes no other action.

and so on.

The next step is *analysis and estimation*. Each team member is
responsible for analyzing and estimating one or more features. She has
to come up with a plausible rough design, and estimate how long it will
take to implement.

Where possible, she should come up with *two* such plans: one for doing
the whole feature, and one that obeys the 80/20 rule by providing part
of what's been asked for with much less effort.

Analysis and estimation presupposes some sort of overall design for the
system as a whole. For example, it doesn't make sense to say, "We'll
create a plugin to handle communication with the new orbiting mind
control laser," unless the application has some sort of plugin system.
If it doesn't, creating one is a task in its own right (probably a large
one). We'll talk more about software architecture in a later episode.

Once everything has been estimated, it's time to prioritize, because
there's always more to do than there is time to do it. The easiest way
to do this for medium-sized projects and teams is to draw a 3×3 grid on
a whiteboard. One axis is "effort", broken down into "small", "medium",
and "large". The other is "importance", broken down into "low",
"medium", and "high". Each feature's name is put on a sticky note, and
then the sticky note goes into one of the nine boxes on the grid:

![Prioritizing Work]({{ site.github.url }}/fig/prioritize.png)

Once this has been done, it's easy to draw a diagonal line on the grid
and throw away everything below it—after all, anything that's rated
"high effort" but "low importance" isn't worth doing. Conversely,
anything that's high importance and low effort definitely belongs in the
plan.

But then there are the diagonal boxes. Should the team try to do one
important, high-effort feature, or tackle a handful of things that are
less important but easier? Whatever they choose, it's critical that they
*don't* shave their time estimates to make things fit. Yes, everyone
wants to aim high, but promising something and then failing to deliver
it on time is worse for everyone than be honest up front and saying, "We
can't get that done."

It's even more important that the *project manager* doesn't shave the
developers' estimates. She's the person responsible for making sure
things get built on time and to spec. One way to look at it is that the
product manager owns the feature list, while the project manager owns
the schedule.

If she starts shaving or squeezing estimates, developers will start
padding them. In response, the project manager will cut them back even
more, until all the numbers are just so much science fiction. Lazy or
timid developers can betray this trust by over-estimating, but even
minimal time tracking will catch that sooner rather than later.

Once the features have been picked, it's the project manager's job to
assemble them into a schedule showing who's going to do what, and when.
The real purpose of this schedule is to help the team figure out if
they're late, and if so, by how much, so that they can start cutting
corners early on.

A common way to do this is to keep a *burn-down chart*, which compares
the plan with reality on a day-by-day or week-by-week basis. If and when
a gap opens up, the team can either figure out when they're actually
going to be done, and move the delivery date back, or go back to the 3×3
grid to figure out what they can drop or scale back to meet the current
deadline.

This, by the way, is why it's useful to have people estimate both the
full feature, and an 80/20 version. If and when time is running short,
it may be possible to switch tracks and deliver most of the value with
much less effort. The right time to think about this is the start of the
project, when people are rested and relatively relaxed, not six weeks
before a major conference deadline when tempers are already frayed.

In order for any of this to work, developers have to be fairly good at
estimating how long things will take.

That comes from experience, but also from careful record keeping. Just
as runners and swimmers keep track of their times for doing their
favorite distances, good developers keep track of how long it takes to
build X or fix Y so that they'll be able to do a better job of
estimating how long the next one will take.

In fact, whether or not a developer keeps track of their stats is a good
way to tell how serious they are about their craft in an
interview—something that would-be developers should keep in mind.

Going back to the original timeline, you may have noticed that design
overlaps estimation, and coding overlaps design. This is deliberate: as
we said at the start of this episode, it's usually impossible to figure
out how to do something without writing some throwaway code.

You may also have noticed that testing starts just as soon as
development. This is critical to the project's success: if it is left
until development is mostly done, it will inevitably be shortchanged.
The consequences are usually disastrous, not least for the team's
morale.

In fact, the members of the team responsible for testing should be
involved in the analysis and estimation phase as well. They should
review every part of the plan to ensure that what the developer is
planning to is testable. Anything that isn't should be sent back to the
drawing board.

Finally, notice that development stops well before the target delivery
date. Ideally, developers should stop adding new code to the project
about two thirds of the way through the development cycle, so that they
can spend the remaining third of the time fixing the problems that
testing turns up.

As soon as they start doing this, or even before, the team should start
"delivering" software by creating and testing installers, deploying it
on a handful of servers, burning ROMs and putting them into the devices
they're supposed to control, and so on. Packaging and delivery are often
just as complex as the software itself, and leaving it until the last
moment will once again usually have disastrous consequences.

The two-thirds point isn't chosen at random. In all too many projects,
that's when the high hopes that the team started with bump into the
reality of over-optimistic scheduling, poor progress monitoring, and
design decisions that weren't reviewed carefully, or weren't reviewed at
all.

The common reaction is to ask the team to buckle down and put in extra
hours. This almost always makes things worse: as study after study has
shown, human beings are only capable of about 40 hours of productive
intellectual work per week. Anything more, and the mistakes they make
because of fatigue outweigh the extra time they're putting in, so that
the project actually slows down.

Evan Robinson's excellent article "[Why Crunch Mode Doesn't Work][robinson-crunch-mode]"
summarizes the science behind this. For example, continuous work reduces
cognitive function 25% for every 24 hours, which means that after two
all nighters, your IQ is that of someone legally incompetent to care for
themselves. The kicker is that, as with other forms of impairment,
people don't realize they're affected: they believe they're still
functioning properly.

One of the key practices in sturdy development is the use of *ticketing*
to keep track of work.

Ticketing tools are often called *bug-tracking systems*, since they are
often used to keep track of bugs that need to be fixed, but
well-organized teams use them as a shared to-do list to manage all kinds
of tasks, not just bugs.

Every task is recorded as a separate ticket, each of which has a unique
number, a one-line summary, its current state, and a longer description
that may include screenshots, error messages, and so on.

It also records who created it and when, and who it's assigned to.

~~~
ID: 1278
Created-By: mummy
Owned-By: wolfman
State: assigned
Summary: Message file reader crashes on accented characters
Description:
1. Create a text file called 'accent.msg' containing the message
 "You vill dream of pümpernickel" (with an umlaut over the 'u').

2. Run the program with 'python mindcontrol.py --all --message accent.msg'.

Program crashes with the message "No encoding for [] on line 1 of 'accent.msg'".
([] shows where a solid black box appears in the output instead of a printable
character.)
~~~
{: .source}

When Wolfman checks in the code that fixes this bug, and the tests for
that fix, he changes the ticket's state from 'assigned' to 'closed'.

If someone later discovers that his fix doesn't actually work, they can
change the state from 'closed' to 'open' (meaning "we need to decide
who's going to work on this") or 'assigned' (meaning "a particular
person is now responsible for working on this").

More sophisticated ticketing systems allow people to record dependencies
between tickets (such as "work can't start on this one until \#917 is
closed"), to estimate how long work will take, to record how long work
actually took, and so on.

They also limit who can change the states of tickets or assign them to
particular people, which is one way to implement particular workflows.

Another key practice in sturdy development is code review. As we said in
an earlier episode, empirical studies have found that this is the single
most cost-effective way to find bugs. It also helps spread understanding
around in teams that don't use pair programming (which most sturdy teams
don't).

Generally speaking, code can be reviewed before it's committed to
version control or after. Most teams prefer pre-commit reviews for two
reasons. First, they prevent mistakes getting into the repository in the
first place, which is better than putting them there and then taking
them out.

Second, if the team agrees that nothing gets committed until it has been
reviewed, it's much more likely that reviews will actually get done. If
changes can be committed, then reviewed later, that "later" may slip and
slip and never come at all.

But wait a second: how can the Mummy review Frankenstein's code *before*
Frankenstein checks it in? Some teams try to solve this problem by
creating one branch per developer, or per feature. The people working in
that branch can check in any time, but review has to happen before code
can be merged with the main line.

Distributed version control systems like Mercurial and Git are
particularly well suited to this kind of development, so it may be come
more popular in future.

For now, though, another common approach is for developers to create a
*patch*. A patch is just a list of the differences between two sets of
files, such as two different versions of the source code for a program.
It also implicitly describes what has to be done to one set of files to
turn it into the other, or vice versa.

Developers can store their patches in the version control system, attach
them to tickets, or submit them to a code review management tool like
ReviewBoard. However they do it, someone else can then look at the
patch, add comments, and give it back to the original developer. In
large open source projects like Python and Firefox, it's common for
patches to be reviewed and updated a dozen times or more before finally
being committed to version control. Newcomers often find this
frustrating, but experience shows that as projects become larger,
"measure twice, cut once" pays off.

So, is sturdy development right for you?

As a rough guide, you should use it when:

1.  Requirements are relatively fixed, or the team has enough experience
    in the problem domain to make estimation and planning possible.

2.  The team is large. If some team members aren't ever going to meet
    others, frequent course changes probably aren't going to be
    possible.

3.  Your customer insists on knowing well in advance exactly what you're
    going to deliver and when. Avionics software and control systems for
    nuclear power plants are extreme examples, but there are many other
    situations in which stakeholders genuinely do need to know exactly
    what's going to be ready to use this time next year.

In practice, agile and sturdy development are more alike than their most
passionate advocates like to pretend. Sturdy teams often use continuous
integration systems and test-driven development, while agile projects
often have an "iteration zero" in which they analyze architectural
options and do large-scale design. That said, there *are* differences.
For example, while both kinds of teams may use ticketing systems,
agilistas tend to see them as a way to keep track of the work backlog,
while teams using sturdy processes focus more on the workflow and
responsibility aspects.

What really distinguishes successful teams and projects from
unsuccessful ones isn't any specific set of practices, but humility.
Most people would rather fail than change; good developers are ones
who are willing to say, "What we're doing now isn't working, let's try
something else." This doesn't mean jumping on every fashionable
bandwagon that rolls by; instead, it means taking an honest look at
what's going wrong, and being brave enough to try something new.

{% include links.md %}
