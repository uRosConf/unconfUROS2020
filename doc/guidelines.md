## High level guidelines for decentral production scripts

_Mark van der Loo, 28-04-2020_

Perhaps this is not really a hackathon topic, but hear me out.  There are many
issues to think about when developing and deploying scripts in production.
(Local) guidelines to do so are often detailed and hard to follow. 

I would propose to have a few simple rules that are **easy to understand** and
**easy to check**. This could help statisticians in production environments to
create better software without having to memorize long and detailed documents.

Preferably, there will be say, 5-10 of these rules, fitting on a single sheet of
A4 paper.


### Some examples.

Here are some rough examples of rules that I can think of. They need not be in the
final version of the document.

1. A script must run on a new version of the data, without changing it.

**Rationale.** This forces abstracting away things like year, quarters, or other things
that may depend on time. It also forces to externalize things like the possible levels
in a classification as classifications may change.

2. A script are under version control. There is just one version for each current script.

**Rationale.** Error tracking, who did what, sharing via a central reporitory.

3. A script must be reviewed by a senior programmer with little or no knowledge
of the statistic being produced.

**Rationale.** Is the script transferable between authors?

4. When R, or one of its packages are updated, problems can be detected automatically.

**Rationale.** This forces automatic testing and testability.


### How to do it

If enough people are interested we can do some breakout-sessions where we first brainstorm
about all kinds of demands, and then filter and summarize to something compact and practical.



