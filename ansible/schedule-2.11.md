# Ansible-3.0.0 Schedule and Preview of 4.0.0 Schedule

## Background

### Versioning

We're switching from our traditional version numbering to a semantic version scheme.  Major releases (roughly every 3-4 months) will be new major versions with potential backwards incompatibilities.  Minor releases (roughly every three weeks) will contain bugfixes and backwards compatible new features.  Micro releases will be infrequent and contain only bugfixes.

Ansible-3.0.0 is roughly equivalent to what Ansile-2.11.0 would have been.


### What are release blocking issues?
  
The ansible-3.0.0 release will be based on ansible-base-2.10, just like ansible-2.10 is.  So I don't think there will be many problems that can rise to release-blocking status.  Any problems with ansible-base will also be present in ansible-2.10 so they won't actually be regressions.  If the released ansible-base-2.10 is really screwy at the time, though, (like it fails to find any of the collections) then we might not want to release until that is fixed even though it technically prevents finding the collections in ansible-2.10 as well.  I think that risk is extremely low.


### Would we slip if certain collections slipped?

Let's say that community.general slips its 2.0.0 release to 2021-02-02.  Would we slip the Ansible release cycle so that we can include community.general-2.0.0 release or would we include the old version of community.general?

I would vote slip.

### Can we use this release schedule with few milesstones for Ansible-3.0.0 and have more milestones for 4.0.0?

* On the one hand, having the same number of milestones gives consistent expectations for users and collection owners as to when to hit certain milestones.
* On the other hand, this release is unlikely to have any blockers whereas the ansible-4.0.0 release will upgrade to the ansible-core-2.12 release so there's a much greater chance of blocker bugs being discovered in the 4.0.0 release than in this one.
  * Additionally, the 4.0.0 release would need to give the ansible-core team time to fix any blockers found, meaning that we need to make pre-releases using ansible-core-2.11 betas and rcs.

I advise that we have a different number of milestones for 3.0 and 4.0.

  
## Proposed Schedule for Ansible-3.0

This release is intended to bring in new releases of collections with potential backwards incompatibilities

2021-01-xx: Release of community.general-2.0.0 and community.networking-2.0.0
2021-02-02: Ansible-3.0.0-beta1 (feature freeze.  collection X.Y numbers are recorded and not updated)
2021-02-09: Ansible-3.0.0-rc1 (final freeze.  Additional changes only to fix blocker bugs.  Requires a new rc)
2021-02-16: Release of Ansible-3.0.0


## Proposed **Extremely Tentative** Schedule for Ansible-4.0.0:

**Extremely Tentative** This schedule is by no means final.  The ansible schedule could change.  The ansible-core schedule could change.  It is given to show how we need more pre-releases when the ansible package is rebasing to a new version of ansible-core.

This release is intended to bring in the new ansible-core package as a dependency

**(AC)**: ansible-core package, releases on Mondays
**(AN)**: ansible package, releases on Tuesdays


---

**(AC)** 2021-02-12 - 2021-03-02 ansible-core-2.11 freezes for various priority components

**(AC)** 2021-03-02 - 2021-03-26 ansible-core-2.11 betas
**(AN)** 2021-03-03 - ansible-4.0.0 alpha1 (biweekly: goal find bugs in the integration with ansible-core)
**(AN)** 2021-03-17 - ansible-4.0.0 alpha2

**(AC)** 2021-03-29 - 2021-04-26 ansible-core-2.11 rcs
**(AN)** 2021-03-30 - ansible-4.0.0 alpha3
**(AN)** 2021-04-13 - ansible-4.0.0 alpha4

**(AC)** 2021-04-26 ansible-core-2.11 release
**(AN)** 2021-04-27 ansible-4.0.0 beta1 (weekly: goal allow collection owners to get set for our release)
**(AN)** 2021-05-04 ansible-4.0.0 beta2

**(AN)** 2021-05-11 ansible-4.0.0 rc1 (weekly: goal give end users a chance to test and tell us of any blocker bugs)
**(AN)** 2021-05-18 ansible-4.0.0 release