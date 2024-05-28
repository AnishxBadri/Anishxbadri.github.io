+++
authors = ["Stuart Broad"]
title = "Git Shit: Origins"
date = "2024-05-27"
description = "Git origin story"
tags = [
    "Git",
]
draft = true 
+++

On April 3rd, 2005, Linus Torvalds released a Linux kernel release candidate, 2.6.12-rc2. While the
release candidate itself was relatively unremarkable, consisting of just a few bug fixes, it became
significant for what it represented: the last Linux kernel release before the adoption of Git.

## Stone Age: Linus as a Version Control Service

Initially, Linus-as-a-version-control-service, aka Linus himself, was the preferred version control
tool for the Linux kernel. Tarballs and patches would be sent by developers to a select set of
Linus's dependable lieutenants. The fixes that made it through the vetting process would be
forwarded to Linus. Ultimately, Linus would manually add them to his own source tree before cutting
the release.

While this manual workflow seems inhumane to us today, Linus at the time considered this woprkflow
to be superior to the altneratives namely CVS. No not the pharamacy you idiot. CVS (Concurrent
Versions System). It employed a centralized model, where a single repository stored all project
files and revbisions, allowing developer to check out, modiy and commit changes. Despite its
popularity, CVS had limitations, including difficulties with branching and merging, limited support
for dsitributewd development, and vulnerability to data corruption. 

One of CVS's prominent critics was Linus himself. Linus believed that it was essential for every
Linux developer to have a separate, isolated copy of the repository so they could work on their own
branches, considering the large number of Linux developers worldwide. This made work easier offline
and also helped with internal politics, since each developer could submit anything they wanted to
their own repository and then had a chance to show the community that their modifications were
worthwhile. This stopped the single repository from being gatekept by a small group of authors with
commit access.

## Medieval Era: BitKeeper

Enter Larry McVoy. Larry McVoy, founder of BitMover, [proposed BitKeeper to the Linux Community in
1998](https://lkml.org/lkml/1998/9/30/122). BitKeeper was radically different from any of its
contemporaries. In his pitch for BitKeeper, McVoy highlighted several key features that set it apart
and whose inspiration we can clearly see in Git:
    
1. Distributed Source Management:

    * BitKeeper: Each user had their own repo, embracing a distributed model 
    * Git: Git also follows a distributed model, where every user has a complete copy of the
      repository, allowing for offline work and independent development.

2. Change Sets:
    
    * BitKeeper: Introduced comprehensive change sets, containing detailed information about
      changes, their locations, revision history, and metadata.
    * Git: Git employs commits as its fundamental unit of change, which serve a familiar purpose to
      BitKeeper's change sets. Commits in Git contain metadata such as author information,
      timestamps, commit messages and references to parent commits, providing a comprehensive
      record of changes.

3. Line of Development (LOD):

    * BitKeeper: Introduced the concept of LODs, which functioned as flexible branches that didn't
      necessarily need to explicitly be created.
    * Git: LOD's are just like Git branches but with better branching and merging capabilities. 

Although Linus admired BitKeeper, his 2002 decision to use the program internally for Linux caused a
great deal of controversy on the Linux Kernel Mailing List.

Controversy? You mean beef? Like Kendrick and Drake? Did Linux community members call Larry McVoy a
pdf file?

Well not really, more like disagreement I guess. You see when Larry McVoy developed BitKeeper, it
was a component of a closed-source for-profit project called BitMover. Although BitKeeper's free
community edition may be used, it had a restrictive license. The community version allowed
developers to use the tool for open-source projects only if weren't participating in developing a
competing version control systems for the duration of their use of BitKeeper plus one year. This
struck a nerve amongst open source developers especially the Linux community who viewed this
restriction as a cardinal sin. They viewed that Linux's open, collaborative approach as a
technically and morally superior way to build software.

Unlike the Linux community, Linus a had more practical view of the matter. He just wanted the best 
possible tool irrespective of its origin.



## Modern Era: Git It always amazes me how two era-defining technologies, JavaScript and Git, were
written in about 2 weeks. While git is a work of art, JavaScript in my opinion, is a cesspool of dog
shit. JavaScript was written in about 10 days, and it shows. Maybe if Brandon Eich spent the
entirety of two weeks he could have come up with something better, but I digress.


## References 


[BitKeeper, Linux, and licensing disputes: How Linus wrote Git in 14 days](https://graphite.dev/blog/bitkeeper-linux-story-of-git-creation)

[Larry McVoy BitKeeper pitch](https://lkml.org/lkml/1998/9/30/122)

[After controversy, Torvalds beigns work on "git"](https://www.infoworld.com/article/2669670/after-controversy--torvalds-begins-work-on--git-.html#:~:text=week%20after%20a-,licensing%20dispute,-forced%20Torvalds%20to)

{{< css.inline >}}

<style>
.canon { background: white; width: 100%; height: auto; }
</style>

{{< /css.inline >}}
