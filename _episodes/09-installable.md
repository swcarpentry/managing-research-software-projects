---
title: "Make the Project Installable"
teaching: 5
exercises: 10
questions:
- "How can I make it easier for people to install my software?"
objectives:
- "Explain what semantic versioning is and why it should be used."
- "Identify two things that can make software hard to install."
keypoints:
- "Use semantic versioning (`major.minor.patch`) to identify software versions."
- "Make old versions of software available."
- "Do not require root permissions or other special privileges to install software."
- "Do not use hard-coded paths in software."
---

*   Version your releases
    *   Semantic versioning: `major.minor.patch`
    *   Release date versioning: `yyyy.vv`
*   Update the version number every time you release a change (however small)
    *   Tempting not to do a full release when "it was just a little change"
*   Make old versions available
*   Do not require root or other special privileges
    *   Users may have this on their laptop, but probably don't have it on the cluster
*   Eliminate hard-coded paths in the software
    *   `/Users/kermit/run_5/data` probably doesn't exist on other people's machines...

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
