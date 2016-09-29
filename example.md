## Code Review for Operations

* Spencer Krum, IBM
* @nibalizer



## Things I am Involved In

* OpenStack
* DevOpsDays PDX
* SeaGL
* Open Infrastructure Day @ SCaLE
* VoxPupuli



## OpenStack Fast Facts

Note:

* ~600 git repos
* 20k commits / 6 mo
* 100k reviews / 6 mo



## Vocab

Note:

* Review(noun): A proposed change to code
* Change(noun): A proposed change to code
* Robot(noun): Some kind of automated process
* Review(verb): A human or robot vote on a change
* Land(verb): A proposed change merging with mainline



## Things we use code review for

Note:

* Changes to daemons
* Configuration of daemons
* Changing users on servers
* Changing packages, files, services
* Changes to our image builds
* Docs



## (More)Things we use code review for

Note:

* Test definitions
* Creating Git repositories
* ACLs for git
* Registering irc channels
* Mapping 'review created' events to irc channels
* Specifications for future work




## (Even More)Things we use code review for

Note:

* Candidacy for elected positions
* Mapping between repositories and jobs
* Releases
* Adding new dependencies
* Grafana dashboards
* Meeting calendar



## Why do People Do Code Review


Note:

* Less defects
* Wider understanding of code
* Slows your brents


## Infrastructure as Code




## Organizational Changes

* Merge speed is an issue <!-- .element: class="fragment" -->
* Auditability becomes huge<!-- .element: class="fragment" -->
* Access control moves from unix to your vcs<!-- .element: class="fragment" -->
* Testing will have less coverage<!-- .element: class="fragment" -->
* Small changes can have huge impact -> stressful<!-- .element: class="fragment" -->
* Many approve -> consensus<!-- .element: class="fragment" -->



## Human Behaviour Changes



## Yolo

Note:

    With any 2 person approval proccess this is true, but it is particularly difficult in IoC environments

    1st person can kinda just be like 'sure, looks good' then the second person is the one who is really on the hook for verifying the code before it goes.
    1st person isn't really required to do a deep review, 2nd person is disincentivized from approving second because blowback sorta falls on them

    The opposite can also be true. That second person can be like 'well the author wrote it and the first reviewer liked it so its probably good and WHAM'

    Imagine for a second how bad it can be when these two people meet on a review.



## Chickens and Pigs

Note:

    One of the reasons cited for dropping the C&P analogy was it didn't leave room for the knowlegeable expert.

    Having an outside expert propose a patch or review a patch can be extremely useful

    Note that they can have laser focus, so remember that the pigs role is still to take the wide view

    We had our gerrit expert propose a change and we approved it like 'sure buddy', then found out we'd opened up a security vulnerability



## WIP Changes

Note:

    This allows you to get early feedback.
    This allows you to go on vacation and somone else can pick it up



## Silence Means No

Note: 

    Giving a -1 review might be what someone is thinking. But the belief that there are bugs in the thing, or the general
    desire not to have that change in the repository will sometimes be realized as someone just refusing to review a
    change.

    "The direction here is wrong"
    "I don't have time to do it right now but we need to that right"




## Forcing the Issue

Note:

    For whatever reason, the team is not agreed on a solution, and pressure is on. One individual or faction wants to
    wait and think, or come up with something elegant. Another wants to quick n dirty.

    The Q&D team can propose that change, then threaten to merge it themselves, or have managers escalate and try to get
    you to do it, or whatever. The point is whomever is resistant to action may be forced to push back hard.

    This can work to your advantage if you're dealing with people who are giving you the 'ignore'.



## Biggest Advantages

* Fewer mistakes
* Audit Trail
* Empowering Chickens
* Spreading knowledge



## Questions?

Spencer Krum, IBM

@nibalizer
