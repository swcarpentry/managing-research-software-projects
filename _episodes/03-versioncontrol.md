---
title: "Use Version Control"
teaching: 5
exercises: 15
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


## Version Control

*   We assume your project is already under version control
    *   If not, this may not be the right course for you
*   We also assume you use version control for everything created by human beings
    *   A major reason for the existence and survival of tools like LaTeX and Markdown
    *   Collaboration would be a *lot* easier if version control systems knew
        how to manage rich document formats...
*   Use a *feature branch workflow*
    *   Designate one branch as the main development branch (typically called `master`)
    *   Create a new branch for each feature from `master`
    *   Only use that branch for that feature
    *   Merge the branch when the feature is done

> ## How Do You Manage Your Repository?
>
> Describe in 3-4 bullet points how you actually manage your version control repository.
> How often are you working on several things simultaneously?
{: .challenge}

> ## Github Flow In Action
>
> - *Before the workshop, make a copy of the [SNDS repository](https://github.com/standage/snds-demo) by cloning it to your local system and pushing it to a new empty repo on Github (something like https://github.com/YourUsername/snds-demo-yyyy-mm-dd). Make sure to collect Github usernames from all participants pre-workshop so you can give them write access to the repo.*
> - *The first pull request will be simple to merge. This will give an opportunity for a brief demo of the code review functionality, comment on particular lines, comment threads, etc.*
> - *The second pull request will likely have a merge conflict. This is now super simple to handle in Github's web interface, and can also be covered in a very brief demo.*
>
> 1. Clone the SNDS repo to your laptop
> 2. Create a new branch with a unique label (such as your last name) and check out that branch.
> 3. Add your name and email address to the `CONTRIBUTORS` file.
> 4. Commit your changes, push your new branch to Github, and open a new pull request to merge your "feature branch" into `master`.
{: .challenge}

{% include links.md %}
