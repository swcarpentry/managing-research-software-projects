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

When a repository with source code, a manuscript or other creative
works becomes public, it should include a file `LICENSE` or
`LICENSE.txt` in the base directory of the repository that clearly
states under which license the content is being made available. This
is because creative works are automatically eligible for intellectual
property (and thus copyright) protection. Reusing creative works
without a license is dangerous, because the copyright holders could
sue you for copyright infringement.

A license solves this problem by granting rights to others (the
licensees) that they would otherwise not have. What rights are being
granted under which conditions differs, often only slightly, from one
license to another. In practice, a few licenses are by far the most
popular, and [choosealicense.com][choose-license] will
help you find a common license that suits your needs.  Important
considerations include:

*   whether you want to address patent rights,
*   whether you require people distributing derivative works to also
    distribute their source code,
*   whether the content you are licensing is source code, and
*   whether you want to license the code at all.

Choosing a licence that is in common use makes life easier for
contributors and users, because they are more likely to already be
familiar with the license and don't have to wade through a bunch of
jargon to decide if they're ok with it.  The [Open Source
Inititative][osi-license-list] and [Free Software
Foundation][fsf-license-list] both maintain lists of licenses which
are good choices.

[This paper][morin-software-licensing] and [this blog
post][vanderplas-licensing] provide excellent overviews of licensing
and licensing options from the perspective of scientists who also
write code.

At the end of the day what matters is that there is a clear statement
as to what the license is. Also, the license is best chosen from the
get-go, even if for a repository that is not public. Pushing off the
decision only makes it more complicated later, because each time a new
collaborator starts contributing, they, too, hold copyright and will
thus need to be asked for approval once a license is chosen.

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
