---
title: "Version Control"
teaching: 5
exercises: 10
questions:
- "How should I manage work using version control?"
objectives:
- "Explain how to use feature branches to manage software development."
keypoints:
- "Use version control for everything created manually, not just code."
- "Create a new branch for each feature."
- "Only use that branch for that feature."
- "Merge and delete the branch when the feature is complete."
---

*   We assume your project is already under version control
    *   If not, this may not be the right course for you
*   We also assume you use version control for everything created by human beings
    *   A major reason for the existence and survival of tools like LaTeX and Markdown
    *   Collaboration would be a *lot* easier if version control systems knew
        how to manage rich document formats...
*   Use a *[feature branch workflow]({{"/reference/#feature-branch" | absolute_url}})*
    *   Designate one branch as the main development branch (typically called `master`)
    *   Create a new branch for each feature from `master`
    *   Only use that branch for that feature
    *   Merge the branch when the feature is done

> ## How Do You Manage Your Repository?
>
> Describe in 3-4 bullet points how you actually manage your version control repository.
> How often are you working on several things simultaneously?
{: .challenge}

{% include links.md %}
