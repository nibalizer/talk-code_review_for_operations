
.. Code Review for Operations slides file, created by
   hieroglyph-quickstart on Thu Aug 25 09:25:40 2016.


Code Review for Operations
==========================

.. figure:: _static/devopsdays_boston_logo.png
   :align: left
   :width: 300px

Spencer Krum, IBM

August 26th, 2016

@nibalizer

.. note::

   * Who am I
   * What do I work on
   * github
   * published link (bit.ly)


Portland
========

.. figure:: _static/Portland_and_Mt_Hood.jpg
   :align: center


.. CC BY-SA https://upload.wikimedia.org/wikipedia/commons/f/fa/Portland_and_Mt_Hood.jpg


Portland
========

.. figure:: _static/afterthebigone.gif
   :align: center


.. Fair Use Motherboard/Vice


Portland
========

.. figure:: _static/superbugs.png
   :align: center


.. Do i need to be fancy with this?


Me
==

* Portland State University
* Large Trucking Company
* OpenStack Infrastructure Project
* Large Company That Used To Do Printers
* IBM

OpenStack Code Fast Facts
=========================

* ~600 git repos
* 20k commits / 6 mo
* 100k reviews / 6 mo

.. note::
    * openstack development is freaking huge

Code Review
===========


.. code-block:: shell


   Code review is systematic examination (sometimes referred to as peer
   review) of computer source code. It is intended to find mistakes
   overlooked in the initial development phase, improving the overall
   quality of software. Reviews are done in various forms such as pair
   programming, informal walkthroughs, and formal inspections.


From wikipedia


.. note::

   * In researching this, I found out a lot of people are doing post-merge big ol read all the code things
   * focus on code review before merge


Code Review
===========


.. code-block:: shell


   Developing software by proposing changes, then seeking peer review
   and approval of those changes.

.. note::

   * focus on code review before merge


Code Review
===========


1) Review happens pre merge

2) Approver isn't the author

.. note::

   * sans robots


Code Review
===========

0) Code is tested before review

1) Review happens pre merge

2) Approver isn't the author

3) Code is re-tested after approval

4) Code is deployed by a robot

.. note::

   * avec robots


Tools and techniques
====================

Tools:

* Reviewboard
* Gerrit
* GitLab
* Stash
* Github


.. note::

   * Yay OpenSource
   * Ish
   * In order of increasing open source ness
   All:
   * Look at the diff
   * Look at the test results
   Wish:
   * Button to have a spun up docker with the code running
   * Give me a url to hit the api at
   * Give me a python repl or whatever with the library loaded
   What kind of feedback can you give:

   * Some allow you to write messages "Great Patch!"
   * Some allow inline comments
   * some allow you to just approve/merge
   * Robot vs Human feedback
   * Some allow you to vote (grid)
   * Some allow you to block merge
   * +1 vs +2: one is 'this looks good but I am not in the approver group' and the other is 'this looks good an i am in the approver group'

   Post Feedback:

   Author proposes new patchset
   Some systems destroy the original patchset

   Gerrit for instance allows you to see what patchset #3 was, and who said what about it.
   Reviewers can then look at the diff between PS3 and PS4 and do a much quicker review. (I liked the code before, and I just wanted this one thing done, ok that is done now cool +2)

   Access Control

   * Who can comment
   * who can approve
   * Who can rerun the tests
   * Who can block the commit from landing
   * Who can update the commit


Tools and Techniques
====================

Techniques:

* Two Pass System
* First pass: Is there anything obviously wrong with it?
* Second pass: Is this good code?


.. note::

   * Jezz humble 'we cant know it will work, but we can show it has known failures and issues'
   * Second pass is pretty subjective
   * Second pass is an effort spectrum:
     ** you're smart, approved without reading
     ** read and the code looks ok
     ** Look at docs for the libraries in play.. are you using it correctly?
     ** Run the code myself
     ** Try to write it a different way, see if it can be simpler or whatever


Tools and Techniques
====================

Questions to ask:

* Does this conflict with other work going on?
* Does it follow the patterns in the code around it?
* Should this be refactoring code as well?
* Is this patch too big?


The Game
========


* Small patches land, big patches don't
* People beg for reviews
* People will make a plan, write it and land it quickly
* People will learn who the soft touches are, and hassle them
* Lots of time spent reviewing = less patches
* Sprinting + Review workflow = hard


.. note:: 

    If the only way to get code into the repository is to get it approved by other people, certain things emerge from that, which then influence behavior.


Why do People Do Code Review
============================


* Fewer defects
* Developers share knowlege, responsibility
* Limits the impact of a 'Brent'
* Brings up the other developers
* Creates Audit trail
* Encourages 'tests always passing'


.. note::
    * encourages in two ways: 
      1) the test passing is looked at, no more push-thrashing
      2) no one wants to waste other peolpes time, they feel bad



References
==========

* All OpenStack Infra repos: http://git.openstack.org/cgit/openstack-infra/
* ansible-puppet role: http://git.openstack.org/cgit/openstack-infra/system-config
* Apply test: http://git.openstack.org/cgit/openstack-infra/system-config/tree/tools/apply-test.sh
* OpenStack CI http://docs.openstack.org/infra/openstackci/
* OpenStack Stats: http://stackalytics.com
