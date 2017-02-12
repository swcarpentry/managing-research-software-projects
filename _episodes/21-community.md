---
title: "Build a Community"
teaching: 5
exercises: 10
questions:
- "How can I turn a project into a community?"
objectives:
- "Identify the two biggest barriers to contribution in open source projects."
- "Explain how to choose the primary medium of discussion for a project."
- "Describe common communication pitfalls in open projects."
keypoints:
- "The two biggest factors affecting participation in open projects are ease of setup and warmth of response to first contribution."
- "Specify a contributor code of conduct for your project."
- "Use one primary channel for communication."
- "Avoid common communication pitfalls."
---

*   Treat every user as a potential contributor
    *   Makes it more likely that others will use your software
    *   Increases the odds of survival for your work when funding runs out or you move on
    *   More likely to impact traditional academic metrics (i.e., citations)
*   [Steinmacher][steinmacher-barriers] identified two main barriers to contribution in open projects
    *   How easy is it to get set up?
    *   How friendly was reception of first contribution?
*   Every project should include a contributor code of conduct
    *   And every project leader should think about [what it's like to be in a vulnerable group][ride-like-a-girl]
    *   Use [Contributor Covenant][contributor-covenant] by default
    *   Make the process for complaint, appeal, and adjudication *very* clear
        *   And make the first point of contact very clear as well
    *   Needs:
        *   Incident response plan (i.e., who does what when an incident occurs)
        *   Widespread promotion (people have to know it exists and where to find it)
*   Most important next step is to manage communication
    *   Small projects converge on one channel (i.e., issues, mailing list, Slack)
        *   "Someone mailed me your tweet about the Slack discussion so I filed a GitHub issue about updating the Google Doc. Wait, why are you crying?"
    *   Strongly prefer email for general discussion: ubiquitous, threaded, and asynchronous
        *   But only if publicly archived
        *   Point-to-point email makes key information unfindable and fosters cliques
    *   And discussion threads on issues for specific topics (to avoid overwhelming general channel)
*   Use video conferencing and in-person meetings to build community, not to share information
    *   People can read faster than you can talk
*   [Avoid common pitfalls][producing-oss-pitfalls]
    *   Don't post without a purpose
    *   Don't rehash previous discussion
        *   Summarize in blog posts or web pages and point people at those
    *   Avoid bikeshedding
        *   "The smaller the problem, the longer the debate"
    *   Throttle discussion
        *   One post per person per topic per day
*   [Recurse Center's social rules][recurse-social-rules]
    *   No feigning surprise
    *   No "well, actually"
    *   No back-seat driving
    *   No subtle -isms
*   Don't be afraid to [market your project][kuchner-marketing]
    *   If it really is good, you should tell people about it
    *   Your papers are your advertisements
        *   Make the main paper(s) you want people to cite obvious, in the documentation and in a CITATION file alongside the README
        *   If there isn't a paper yet, get agreement on what's needed for a "code paper" (journals like [JOSS](http://joss.theoj.org/) and [JORS](http://openresearchsoftware.metajnl.com/) have clear guidelines and checklists)
        *   Keep planning for future papers and how people should be credited for their work so that the community remains engaged and committed (see [one example](http://ivory.idyll.org/blog/2015-authorship-on-software-papers.html) of an open discussion of this)
    *   Your grant proposals are your product

> ## Code of Conduct
>
> Add the Contributor Covenant or some similar code of conduct to your project.
> (Do *not* create one of your own.)
> What is the process for complaint, appeal, and adjudication?
{: .challenge}

> ## Channels
>
> 1.  What is your project's primary communication channel?
> 2.  Why and how was it chosen?
> 3.  What discussion(s) take place in other channels?
> 4.  Why?
> 5.  How easy or hard is it for a newcomer to find where things are being discussed?
{: .challenge}

{% include links.md %}
