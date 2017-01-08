---
title: "Introduction"
teaching: 5
exercises: 10
questions:
- "What are the key differences between research software and 'normal' projects?"
- "What does 'done' look like for a research software project?"
- "What are the goals of this class?"
objectives:
- "Compare and contrast research software projects and 'normal' software projects."
- "Name and explain key features of a mature research software project."
keypoints:
- "Requirements for small research software projects are typically emergent."
- "Research software is 'good enough' when people other than its authors can use it with confidence and extend it with reasonable effort."
---

*   Key differences between research software and "normal" projects
    *   Requirements may be either:
        *   Discovered as we go along (exploring)
        *   Relatively stable (engineering)
    *   Problem is *subtle* as well as *complicated*
        *   Control flow may be very simple...
        *   ...but figuring out exactly what coefficients and indexes to use can be very hard
*   What does "done" look like?
    1.  Software can be used by people other than original authors
        *   Reproducibility meaningless without this
    2.  Reasonably confident that results are correct
        *   As trustworthy as physical experiment
    3.  Small changes and extensions are easy
        *   I.e., researchers can safely make small changes to code
    4.  Fast enough to be useful
    5.  Can be maintained by people other than its original author(s)
        *   I.e., it is *sustainable*
*   For our purposes:
    *   3x6: three people for six months
    *   Contributors are frequently time-slicing other projects
    *   "Everybody makes coffee"
*   Goals for this class
    *   Understand how to go from ad hoc solo project to reliable small-team project

> When life gives you lemons, think carefully if you want to tend a lemon tree garden forever.
>
> – [Daniel Schauenberg][quote-schauenberg]
{: .quotation}

> ## Create a Value Proposition for Your Project
>
> Fill in the template below for your current project.
>
> 1.  For *[description of target users*]
> 2.  who want to *[statement of their need(s)]*,
> 3.  *[project name]*
> 4.  provides *[statement of key benefits]*.
> 5.  Unlike *[name of alternative solutions(s)]*,
> 6.  our project enables users to *[key differentiator]*.
{: .challenge}

> ## Describe How Your Project is Managed
>
> Write a short point-form description (5-6 bullets) of how your current project is managed:
>
> 1.  Who uses the software?
> 2.  How?
> 3.  How do they find the software?
> 4.  How do they set it up?
> 5.  Who decides what to change and when?
> 6.  How are decisions and changes circulated?
{: .challenge}

====

---
title: "Research Software Engineers"
teaching: 5
exercises: 10
questions:
- "What is a research software engineer?"
objectives:
- "Explain what research software engineers do and don't do."
keypoints:
- "Research software engineers usually have advanced degrees in a research area, but are no longer principally doing research."
- "Research software engineers design, write, test, and maintain software."
- "Research software engineers need to understand languages, version control, build and test tools, performance tools, packaging, and lifecycle management."
---

*   [What is a research software engineer][what-is-rse] (RSE)?
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
*   What do RSEs need to know?
    *   Programming language(s) - in more depth than most of their research colleagues
    *   Version control - ditto
    *   Build and test tools - often the only one on their team doing any of this
    *   Performance analysis and tuning - ditto
    *   Packaging and deployment - ditto (and then some)
    *   Software lifecycle management - often de facto process owners
        *   What needs to be done?
        *   Why?
        *   Who's doing it?
        *   When is it due?
        *   What state is it in (i.e., are we done yet)?
        *   Where is everything?
        *   How do we do things?

> ## Are You an RSE?
>
> Score yourself using the questions below.
>
> 1.  Are you employed to develop software for research?
> 1.  Are you spending more time developing software than conducting research?
> 1.  Are you employed as a postdoctoral researcher,
>     even though you predominantly work on software development?
> 1.  Are you the person who does computers in your research group?
> 1.  Are you sometimes not named on research papers
>     despite playing a fundamental part in developing the software used to create them?
> 1.  Do you lack the metrics needed to progress your academic career,
>     like papers and conference presentations,
>     despite having made a significant contribution through software?
{: .challenge}

> ## What Skills Do You Already Have?
>
> What do you use for each of the following?
> ("Nothing yet" is a perfectly good answer.)
> What fraction of what you think you need to know do you believe you actually know?
>
> *   Programming language(s)
> *   Version control
> *   Build tools
> *   Testing tools
> *   Performance analysis tools
> *   Packaging and deployment tools
> *   Software project management tools
{: .challenge}

====

---
title: "Version Control"
teaching: 5
exercises: 10
questions:
- "FIXME"
objectives:
- "FIXME"
keypoints:
- "FIXME"
---

*   Assume your project is already under version control
    *   If you are not, this may not be the right course for you
*   You may need to meet people halfway if you want your project to grow
*   Your collaborators might not be using it
    *   And they might be right
*   Google Docs for papers
*   Dropbox for files
    *   [Integrates with Git][git-dropbox]
    *   Non-trivial setup...

> …try to explain the notion of compiling a document to an
> overworked physician you collaborate with. Oh, but before that, you
> have to explain the difference between plain text and word
> processing. And text editors. And markdown/LaTeX compilers. And
> BiBTeX. And Git. And GitHub. Etc. Meanwhile he/she is getting paged
> from the OR…
>
> …as much as we want to convince ourselves otherwise, when you
> have to collaborate with those outside the scientific computing
> bubble, the barrier to collaborating on papers in this framework is
> simply too high to overcome. Good intentions aside, it always comes
> down to "just give me a Word document with tracked changes," or
> similar.
>
> – [Stephen Turner][good-enough]

> Google Docs excels at easy sharing, collaboration, simultaneous
> editing, commenting and reply-to-commenting. Sure, one can approximate
> these using text-based systems and version control. The question is
> why anyone would like to…
>
> The goal of reproducible research is to make sure one
> can…reproduce…computational analyses. The goal of version
> control is to track changes to source code. These are fundamentally
> distinct goals, and while there is some overlap, version control is
> merely a tool to help achieve that, and comes with so much overhead
> and baggage that it is often not worth the effort.
>
> [Arjun Raj][quote-raj]

> Normal humans don't work like programmers expect them to
> because programmers haven't built tools that would let them.  
>
> – [Mike Hoye][quote-hoye]

{% include links.md %}

====

---
title: "Choose a License"
teaching: 5
exercises: 0
questions:
- "What licensing information should I include with my work?"
objectives:
- "Explain why adding licensing information to a repository is important."
- "Choose a proper license."
- "Explain differences in licensing and social expectations."
keypoints:
- "People who incorporate GPL'd software into their own software must make their software also open under the GPL license; most other open licenses do not require this."
- "The Creative Commons family of licenses allow people to mix and match requirements and restrictions on attribution, creation of derivative works, further sharing, and commercialization."
- "People who are not lawyers should not try to write licenses from scratch."
---

*   Creative works are automatically eligible for intellectual property (and thus copyright) protection
*   Reusing creative works without a license is dangerous
    *   Because copyright holders could sue you for copyright infringement
*   Every repository (version control or otherwise) should therefore include an explicit license
    *   Usually `LICENSE` or `LICENSE.txt` in root directory
*   Clearly states under which license(s) the content is being made available
    *   Plural because code, data, and text may be covered by different licenses
*   Important to decide early
    *   Otherwise, each time a new collaborator starts contributing,
        they will hold copyright on their work
        and will thus need to be asked for approval when a license is chosen
*   A few licenses are by far the most popular
    *   Choosing a common license makes project more intelligible
    *   **Don't write your own** (even if you are a lawyer)
*   Common licenses
    *   [Open Source Inititative][osi-license-list] license list
    *   [Free Software Foundation][fsf-license-list] license list
    *   [choosealicense.com][choose-license] will help you find a license that suits your needs
*   For code:
    *   **MIT/BSD**: do whatever you want as long as you cite the original source, and we accept no responsibility if things go wrong
    *   GPL: as above, but changes must be distributed
*   For data and text:
    *   **CC-0**: public domain (for data)
    *   **CC-BY**: do whatever you want as long as you cite the original source (for papers)
    *   Other restrictions all inhibit legitimate use cases
        *   -ND: no derivative works
        *   -NC: no commercial use (without explicit permission)
        *   -SA: share-alike
*   Considerations:
    *   Do you want to license the code at all?
    *   Is the content you are licensing source code?
    *   Do you require people distributing derivative works to also distribute their code?
    *   Do you want to address patent rights?
*   See [this paper][morin-software-licensing]
    and [this blog post][vanderplas-licensing]
    for overviews from a scientist's point of view

> ## Can I Use an Open License?
>
> Find out whether you are allowed to apply an open license to your software.
> Can you do this unilaterally,
> or do you need permission from someone in your institution?
> If so, who?
{: .challenge}

> ## What Licenses Do My Dependencies Use?
>
> Make a list of the licenses used by the projects that your project depends on.
> Are there any conflicts between them and the license that you have chosen?
{: .challenge}

{% include links.md %}

====

---
title: "Hosting"
teaching: 5
exercises: 10
questions:
- "Where should I host my version control repositories?"
objectives:
- "Explain different options for hosting scientific work."
keypoints:
- "Projects can be hosted on university servers, on personal domains, or on public forges."
- "Rules regarding intellectual property and storage of sensitive information apply no matter where code and data are hosted."
---

*   Where to host code and data?
*   Option 1:  lab, department, or university provides server, manages accounts and backups, etc.
    *   Pro: clarifies who owns what
        *   Particularly important if any of the material is sensitive
            (i.e., relates to experiments involving human subjects or may be used in a patent application)
    *   Con: cost often higher than commercial services
    *   Con: longevity
        *   Someone who has spent ten years collecting data wants it to be available 10 years from now
        *   That's well beyond the lifespan of most of the grants that fund academic infrastructure
*   Option 2: purchase a domain and pay an Internet service provider (ISP) to host it
    *   Pro: gives the individual or group more control
    *   Pro: sidesteps problems that can arise when moving from one institution to another
    *   Con: requires more time and effort to set up than other options
    *   Con: may not be allowed
*   Option 3: public host service
    *   [GitHub][github], [GitLab][gitlab], [BitBucket][bitbucket], [SourceForge][sourceforge], …
    *   All provide web interface to
        *   Create, view, and edit projects
        *   Communication and project management tools (issue tracking, wiki pages, email, code reviews)
    *   Pro: economies of scale
    *   Pro: network effects (potential collaborators probably already know how to use them)
    *   Con: public (unless you pay)
        *   And even then, out-of-institution/out-of-country hosting can be problematic
    *   Con: can be shut down, purchased, etc.

> ## Institutional Barriers
>
> Sharing is the ideal for science,
> but many institutions place restrictions on sharing,
> for example to protect potentially patentable intellectual property.
> If you encounter such restrictions,
> it can be productive to inquire about the underlying motivations
> either to request an exception for a specific project or domain,
> or to push more broadly for institutional reform to support more open science.
{: .callout}

> ## Sharing Code vs. Sharing Publications
>
> FIXME:  Discuss how code repositories
> differ from services like [arXiV][arxiv] and [figshare][figshare].
{: .callout}

> ## Can My Work Be Public?
>
> Find out whether you are allowed to host your work openly on a public forge.
> Can you do this unilaterally,
> or do you need permission from someone in your institution?
> If so, who?
{: .challenge}

> ## Where Can I Share My Work?
>
> Does your institution have a repository or repositories that you can
> use to share your papers, data and software?
{: .challenge}

{% include links.md %}

====

---
title: "Automate Development Tasks"
teaching: 5
exercises: 10
questions:
- "FIXME"
objectives:
- "FIXME"
keypoints:
- "FIXME"
---

*   DRY: Don't Repeat Yourself
    *   Usually applied to nouns (code)
    *   Just as true for verbs (actions)
    *   The only thing you can accomplish by typing something repeatedly is to get it wrong
*   Use a build manager
    *   [GNU Make][gnu-make] defined the category, but depends on native shell commands
    *   [CMake][cmake] is a meta-tool that creates build files for multiple systems
    *   [SCons][scons] and similar tools define build rules in a full-blown programming language
    *   Many more…
*   Originally created to compile multi-file programs efficiently, but can all be used for arbitrary tasks
    *   Run tests, build packages for release, create reports, …
    *   Common pattern: build shell script or utility program, then launch from build file

> ## Create a Task list
>
> 1.  If your project already uses a build manager,
>     what tasks are used most often?
> 2.  If your project *doesn't* use a build manager,
>     what are the first few tasks you should automate?
{: .challenge}

> ## Self-Documenting Build Files
>
> The default target in a build file (e.g., `make` with no parameters)
> should print a list of available commands.
> Look at the `Makefile` in this repository to see how this works,
> then modify the build file for your project to do so as well.
{: .challenge}

{% include links.md %}

====

---
title: "Checklists"
teaching: 5
exercises: 10
questions:
- "FIXME"
objectives:
- "FIXME"
keypoints:
- "FIXME"
---

*   A checklist is a build file meant to be executed by human beings
    *   *[The Checklist Manifesto][gawande-checklist-manifesto]*
        describes how use of checklists cuts fatalities in surgery significantly,
        along with many other examples
*   Use them for anything that *can't* be done automatically by a machine
*   Keep in version control
    *   Ask every new contributor/user to use *and give feedback*
*   Include a contact email address in every checklist

> ## Checklist for First Day of Software Carpentry Workshop
>
> 1.  As learners arrive,
>     ask them to connect to the network
>     and check that they have software installed.
> 2.  Remind everyone of the Code of Conduct.
> 3.  Circulate the sign-in sheet and photo release form.
> 4.  Distribute sticky notes.
> 5.  Debug remaining software installation problems.
>     *   If someone can't get software working, pair them with someone who has it working.
> 6.  Remind learners of the workshop's goals and schedule.
> 7.  Remind helpers to mingle as well as answer questions.
>
> Questions or suggestions? Email help@software-carpentry.org.
{: .callout}

> ## Create a Setup Checklist
>
> 1.  Write a short point-form checklist describing the things you do
>     when setting up a new machine to do development on your project.
>
> 2.  How many of the steps in your checklist can be automated using shell scripts or other small programs?
>
> 3.  How will newcomers know if they have completed the steps in the checklist correctly?
{: .challenge}

{% include links.md %}

====

---
title: "Make the Project Describe Itself"
teaching: 5
exercises: 10
questions:
- "FIXME"
objectives:
- "FIXME"
keypoints:
- "FIXME"
---

*   *Robust* is the difference between "works for me on my machine"
    and "works for someone I've never met on a cluster I've never heard of"
    *   Rules are described in [Taschuk's Rules](http://oicr-gsi.github.io/robust-paper/)
*   Have a README that briefly explains what the software does and what its dependencies are
    *   For humans to read *before* installing
*   Tell the user what could be done
    *   Print usage from the command line by default
    *   Include version (discussed below)
*   Tell the user what was *actually* done
    *   Log actions

> ## Write a Usage Statement
>
> Run `make --help` (or something similar) and examine its output,
> then write a similar command-line usage message for your project.
{: .challenge}

> ## Logging
>
> Read the [tutorial on the Python logging library][python-logging-tutorial]
> (or an equivalent tutorial for your preferred language's logging library).
>
> 1.  How do libraries of this kind give users control over what is logged and where?
> 2.  Is this an appropriate level of complexity for your project?
>     If not, what would you use instead?
{: .challenge}

{% include links.md %}

====

---
title: "Make the Project Installable"
teaching: 5
exercises: 10
questions:
- "FIXME"
objectives:
- "FIXME"
keypoints:
- "FIXME"
---

*   Version your releases
    *   Semantic versioning: `major.minor.patch`
    *   Release date versioning: `yyyy.vv`
*   Make old versions available
*   Do not require root or other special privileges
*   Eliminate hard-coded paths in the software

> ## How Do You Version Now?
>
> How many different versions of your project are in use right now?
> How do you know?
> If a user has a problem,
> how will you and they find out which version of the software they have?
{: .challenge}

> ## Where Does Your Software Live?
>
> 1.  What directories does your software add files to when it is installed?
> 2.  What new directories does it create?
{: .challenge}

> ## Hard-coded Paths
>
> 1.  What files does your software read and/or write?
> 2.  How do you know?
> 3.  Which of these are referenced by fixed (hard-coded) paths?
{: .challenge}

{% include links.md %}

====

---
title: "Make the Software Easy to Integrate"
teaching: 5
exercises: 10
questions:
- "FIXME"
objectives:
- "FIXME"
keypoints:
- "FIXME"
---

*   Command-line parameters for commonly-changed options
    *   Also makes program easy to control from shell scripts
*   Configuration files for less frequently changed options
*   Frequently use multiple overlaid configuration files
    *   System-level configuration file created during installation for things like cluster name
    *   User-level configuration file in `~/.programrc` for user's credentials
        *   `rc` suffix is old Unix abbreviation for "resource control"
    *   Job-level configuration file for particular runs

> ## Common and Rare
>
> 1.  What options or parameters does your program use?
> 2.  Which ones are users most likely to set or change?
> 3.  How do you know?
{: .challenge}

> ## Configuration Files
>
> 1.  Can some or all of your program's options be specified in an external configuration file?
> 2.  If so, what data format do those files use?
> 3.  If not, is it worth adding that capability?

{% include links.md %}

====

---
title: "Make the Software Trustworthy"
teaching: 5
exercises: 10
questions:
- "FIXME"
objectives:
- "FIXME"
keypoints:
- "FIXME"
---

*   Not enough to be right - have to be *seen* to be right
*   Include a small test set that can be run to ensure the software is actually working
    *   Not the same as a comprehensive unit test suite for use in development (which you should also have)
    *   Unit tests may take too long to run, and output may not be actionable
    *   Want smaller suite that says "am I set up correctly?"
*   Produce identical results when given identical inputs
    *   Absolutely necessary for reproducible research
    *   Means external control of random numbe generation seeds,
        aggregation order for floating point results,
        dates and times,
        etc.
    *   Probably the hardest thing on this list for many projects

> ## Is This Turned On?
>
> 1.  How can the person who installs your software tell if it is installed correctly?
> 2.  How can the person who *uses* your software tell if it is installed correctly?
{: .challenge}

> ## Out of Control
>
> Under what circumstances could your program produce different answers
> when given what the user believes are the same inputs?
{: .challenge}

{% include links.md %}

====

---
title: "Choose Boring Technology"
teaching: 5
exercises: 10
questions:
- "FIXME"
objectives:
- "FIXME"
keypoints:
- "FIXME"
---

*   Idea discussed in [McKinley's talk][mckinley-boring]
*   Every project has a limited "innovation budget"
    *   Because every new technology introduces risk
    *   And risks interact non-linearly
*   Allow yourself one new tool or practice at a time
*   And (strongly) prefer things that have been around for a long time
    *   Limitations are known
    *   More people likely to know how to work with them
    *   "What's oldest will last longest" (proverb)

> ## Familiarity
>
> List the main dependencies of your project,
> then create a 2x2 grid
> where the X axis is how long has each one has existed
> (weeks, months, years, decades)
> and the Y axis is how long you have been using it
> (same scale).
> How many of your dependencies are in an uncomfortable part of the grid?
{: .challenge}

{% include links.md %}

====

---
title: "Packaging"
teaching: 5
exercises: 10
questions:
- "FIXME"
objectives:
- "FIXME"
keypoints:
- "FIXME"
---

*   Describe dependencies in machine-readable form

> ## Requirements for a Simple Website
>
> ~~~
> Django>=1.9,<1.10
> PyYAML
> requests>=2.0
> ~~~
{: .source}

*    Set up development machines using a package manager
    *   Doesn't guarantee that the file is up to date, but it helps
*   Use the same package description to install software on users' machines
*   Package managers are often painful to work with
    *   Like standards, everybody has their own
    *   Often language-specific
    *   Often complex (because they're solving complex problems)
    *   Focus on libraries - generally don't address extra development tools

> ## Dependencies
>
> Describe your project's dependencies in the format shown above.
{: .challenge}

{% include links.md %}

====

---
title: "Issues"
teaching: 5
exercises: 10
questions:
- "FIXME"
objectives:
- "FIXME"
keypoints:
- "FIXME"
---

*   Issue-tracking tools are often called bug trackers
    *   Well-organized teams use them as a shared to-do list to manage everything
*   Every task is recorded as a separate ticket
    *   Unique ID
    *   One-line summary to aid browsing
    *   Status
    *   Owner (i.e., who's responsible)
    *   Full description that may include screenshots, error messages, etc.
    *   History: who created it when, how it has been modified
    *   Threaded discussion

~~~
ID: 1278
Created-By: mummy
Owned-By: wolfman
State: assigned
Summary: Message file reader crashes on accented characters
Description:
1.  Create a text file called 'accent.msg' containing the message
    "Pümpernickel" (with an umlaut over the 'u').

2.  Run 'python mindcontrol.py --all --message accent.msg'

Program crashes with the message "No encoding for [] on line 1 of 'accent.msg'".
([] shows where a solid black box appears in the output instead of a printable
character.)
~~~
{: .source}

*   More sophisticated systems allow people to:
    *   Record dependencies between tickets
    *   Estimate how long work will take
    *   Record how long work actually took
*   Can be used to make the development lifecycle explicit
    *   I.e., only allow certain state transitions
    *   And notify interested parties of state transitions

![Issue Lifecyce]({{ site.github.url }}/fig/issue-lifecycle.png)

*   Don't worry about any of this until people are actually filing issues
*   Key use: prioritization
    1.  What has to be done right now?
    2.  What should be done soon?
    3.  What can safely be left until later?

> ## What's On Your List?
>
> 1.  What are the top 10 items on your project's to-do list?
> 2.  How sure are you that your collaborators and users would agree with your selection?
{: .challenge}

> ## What's Missing?
>
> Look at the issue lifecycle diagram above.
> What steps or transitions would you add?
> Which ones would you remove?
> Which ones would you make other people responsible for?
{: .challenge}

> ## What's Your Lifecycle?
>
> 1.  What states can your project's issues be in?
> 2.  What state transitions are allowed?  ("Any to any" is a common and acceptable answer.)
> 3.  Who decides when an issue can move from one state to another?
{: .challenge}

> ## How to Write a Good Bug Report
>
> FIXME: links to articles and action to critique a bug report.
{: .challenge}

{% include links.md %}

====

---
title: "Work While You're Asleep"
teaching: 5
exercises: 10
questions:
- "FIXME"
objectives:
- "FIXME"
keypoints:
- "FIXME"
---

*   FIXME: continuous integration
*   FIXME: lint the code as part of running tests

{% include links.md %}

====

---
title: "Choose a Process"
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

====

---
title: "Specify Tolerances"
teaching: 5
exercises: 10
questions:
- "FIXME"
objectives:
- "FIXME"
keypoints:
- "FIXME"
---

FIXME: this is *implemented* as testing, but what you're really doing is deciding on tolerances

{% include links.md %}

====

---
title: "Build a Community"
teaching: 5
exercises: 10
questions:
- "FIXME"
objectives:
- "FIXME"
keypoints:
- "FIXME"
---

*   [Steinmacher][steinmacher-barriers]'s analysis of barriers to contribution
    *   How easy is it to get set up?
    *   How friendly was reception of first contribution?
*   treat every user as a potential contributor
*   add the following to Noble's Rules:
    *   `CONDUCT`: project's social rules
    *   `LICENSE`: terms of re-use
        *   **Use a standard license** (preferably MIT)
    *   `CITATION`: how to cite the software
        *   Get a DOI for the software (see [Zenodo][zenodo])
    *   `CONTRIBUTING`: how to make contributions
        *   Most important documentation is how to set up for development
*   Simultaneously selfless and selfish
    *   makes science easier to evaluate
    *   makes life easier on your colleagues
    *   makes it more likely that others will use (and **contribute to!**) your software
    *   ensures relevancy of your work when funding runs out or maintainer moves on
    *   more likely to impact traditional academic metrics (i.e. citations)

*   general communication
    *   small projects converge on one channel (i.e., issues, mailing list, Slack)
    *   strongly prefer email as lowest common denominator, threaded, and async
        *   aside: throttling
*   video conferencing
*   in-person meetings
*   [avoid common pitfalls](http://producingoss.com/en/producingoss.html#common-pitfalls)

{% include links.md %}

====

---
title: "Mentor"
teaching: 5
exercises: 10
questions:
- "FIXME"
objectives:
- "FIXME"
keypoints:
- "FIXME"
---

*   FIXME: [recalibrate productivity sensors][bartel-recalibrate]
*   FIXME: [managing participants](http://producingoss.com/en/producingoss.html#managing-participants)
*   FIXME: [teaching pair programming](http://csteachingtips.org/tips-for-pair-programming)
*   FIXME: [give your cat a performance review](https://hackernoon.com/a-guide-to-giving-your-cats-their-annual-performance-review-fbf14610305)
*   FIXME: pair programming

{% include links.md %}

====

---
title: "Conclusion"
teaching: 5
exercises: 10
questions:
- "FIXME"
objectives:
- "FIXME"
keypoints:
- "FIXME"
---

*   FIXME: wrap up
*   FIXME: *[Marketing for Scientists][kuchner-marketing]*

{% include links.md %}

====

*   FIXME: pre-commit review
