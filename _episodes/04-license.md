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
    *   Is your license compatible with the licenses of the software you depend on?
        *   E.g., can't use MIT on top of GPL
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
