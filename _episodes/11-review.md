---
title: "Code Review"
teaching: 5
exercises: 10
questions:
- "How can I tell when software is ready to be integrated?"
- "How can I share knowledge within my team?"
- "How can I be more productive when I'm actually writing code?"
objectives:
- "Describe three benefits of code reviews."
- "Explain the difference between pre-commit and post-commit review."
- "Explain what pair programming is and why it improves productivity."
- "Explain when pair programming is best used."
keypoints:
- "Code review is the most cost-effective way to find bugs known."
- "Use pre-commit review."
- "Review code after all mechanical checks have passed."
- "Keep changes short enough to be reviewed in less than an hour."
- "Use code review to share knowledge within the team."
- "Pair programming is the practice of having two people share one computer while writing code."
- "One person is the driver (typing) while the other is the navigator (watching and commenting)."
- "Pairs should switch roles periodically."
- "Pair programming helps spread knowledge."
- "Pair programming is particularly useful for onboarding and difficult tasks."
---

*   Code review is the most cost-effective way to find bugs we know of
    *   *Pre-commit*: review before change is merged into shared branch in version control
    *   *Post-commit*: review after merge
    *   Pre-commit is more beneficial, and is now supported by all major version control systems
*   Code review works best when:
    *   Code has already been checked mechanically
        *   All tests pass
        *   All style rules obeyed
    *   Each review takes less than an hour
        *   Which puts a sharp upper bound on size of change
    *   Focus is on behavior, not appearance
    *   Reviewer has checklist to refer to
        *   Which includes usability as well as correctness
        *   If nobody can figure out how to call a function, it might as well not exist
*   And review includes review of the documentation
    *   Including review of the commit comments, because readable logs matter too
*   Aim is not just to prevent bugs
    *   *Share knowledge*
    *   Ensure a consistent way to solve problems, not just consistent (superficial) style
    *   Detect duplication
*   For adoption, start with "at least one round of code review per feature"
    *   Where a feature is "a body of work that took less than a week"
*   See [Cohen et al][smart-bear-code-review] for more details
*   *Pair programming* is real-time code review
    *   The *driver* does the typing
    *   The "navigator" watches and comments
    *   Every hour or so, the pair switches roles
    *   The navigator is effectively giving real-time code review
*   Benefits
    *   Spreads knowledge around
    *   Helps people pick up new skills
    *   And people are less likely to check Facebook every five minutes if someone else is working with them
*   In practice, most people don't want to do it all the time
*   Save it for:
    *   Onboarding
    *   Particularly hard tasks
    *   Socialization: an hour a day of pairing helps keep the team together

> ## Challenge
>
> Pair up with someone who is comfortable in the language you are using in your project.
> Give them a page of code that you are currently working on to read,
> and read carefully through a page of the code that they are working on.
>
> 1.  What can you not understand about their software without more context?
> 2.  What *can* you understand, and how useful is feedback on that?
> 3.  Did they use any features of the language that you haven't seen before or don't use?
{: .challenge}

<blockquote class="challenge" markdown="1">
## Pair Programming

Solve the two programming challenges below using pair programming.
Switch roles for the two exercises.

{% include problems.md %}
</blockquote>

{% include links.md %}
