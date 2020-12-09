# How to code of conduct

Covering miscellaneous thoughts about codes of conduct within an aggregate project.


## Too restrictive vs too lenient

* Too lenient: Merely saying every upstream must have a CoC can lead to people gaming the system.  I could put in things that are counter to the real goal of promoting an inclusive community and call it a CoC.
* Too restrictive: Saying that all upstreams must use our CoC as their CoC is problematic.  Some upstreams may have their own CoCs, may belong to communities that have different CoC requirements, or may even have legal departments that mandate certain CoCs.


## Interim Policy

Independent ideas:

* Possibly a good starting point for discussion would be "Must be compatible with our code of conduct".  The upstream could still have a more lax CoC than we do but at least they wouldn't be able to demand that people act in a way that is counter to how we tell people to act.

* Look into adopting a list of known good codes of conduct
  * https://geekfeminism.wikia.org/wiki/Code_of_conduct_evaluations
    * No longer maintained but we might be able to find another list which is maintained (CHAOSS?)
    
* initially saying "CoC compatible with Ansible's" and then making a more in depth definition or policy a joint community/D&I effort to sort out?
  * Tasks:
    * What's the minimum that the CoC must cover?
    * Evaluate unknown CoC's for compliance with the minimums.

* We could RECOMMEND collections just point to our CoC. And for those who don't, we'd have to evaluate whether they meet our requiremetns

* Can we require that repositories under ansible-collections use our CoC?
  * This sounds reasonable but there are ramifications.
    * If, as a group, the people doing the work on ansible-collections/community.crypto want to use a different CoC, we need to provide the path for them to move their repo while still being in the ansible tarball.


## In an ideal world...

What would we like an overaching policy to look like?

* Some group (perhaps the D&I working group for us) to evaluate CoC's.
* Published minimum standards for needs to be in a CoC.
* Published additional guidance for writing an outstanding CoC.
* Publish a list of good CoCs


## Issues

* In the phrase, "Compatible with Ansible's CoC", what does "compatible" mean?
  * Initially means "Does not conflict with how we want our community to behave"
  * Eventually we'd want the D&I working group to create a new set of criteria that we can use instead of this vague phrase.

* Evolution of standards
  * As time goes on, D & I will have a better idea of what makes for a good CoC and possibly also ideas for what makes for an acceptable CoC.
  * How do we get the upstream projects to update their CoCs?
  * Would we kick a collection out for not updating to the new CoC?
  * For most things we'd probably grandfather in existing collections.
  * Should have a mechanism to alert people to updates.
  * Major updates to the standards shouldn't happen terribly often

* How should CoC violations in one collection affect the others?
  * Example: someone is banned in community.general.  Does that apply to others collection and ansible as well ?
    * Because of the nature of the ansible package (like a Linux distro, it's an aggregation of other upstream projects), I don't think the ban necessarily transfers.  We couldn't force vmware.vsphere to also ban the contributor, for instance.
    * Would we want to ban them from other collections in our organization (for instance, all of ansible-collections/*)?
      * This probably depends on the circumstances
  * We might want to communicate about what people have violated the CoC as well as circumstances around the incident.
    * But we need to be careful as well.  We don't want this to be done as further punishment (public shaming) but we do want to inform our community of why an action was taken and want to inform other collections in case they are having similar problems and have been hesitating to take action.
    * Rules (so everyone knows that they are being treated equally under the policy) and transparency (so other people can check whether the action makes sense) are important
  * How to deal with shared spaces
    * If I was banned from collections.foo should I still be allowed to discuss things on #ansible? (it's a shared space which all collections can use)


### Cornercases... how we want to handle them and whether our policy does what we want:

* Imagine a code of conduct that exactly matches ours in substance but is not written by us.  Do we accept that?
  * I think we want to
* Imagine a company that has already had their code of conduct pushed upon them by their legal department.  The code of conduct isn't outrageous (It doesn't do the opposite of what we think a coc should do), do we accept that?
  * I think we want to
* Imagine that we have the perfect code of conduct that covers every case imaginable.  Do we accept a collection that has a different coc that is perfect -1?
  * I think it depends on whether the slightly less perfect CoC still satisfies some minimum requirements for a CoC.
* Imagine a code of conduct that is similar to ours but different.  For instance, their enforcement draws slightly different lines than ours.  Do we accept it?
  * I think we want to
* Imagine that Ansible's CoC is not as good as the collection's.  Do we accept it?
  * I think we'd want to


## Observations

* This looks a lot like licensing discussions
  * List of acceptable CoC's like lists of acceptable licenses
  * Protection it offers to users
  * We're early in the stage of CoC development, kind of like licensing was before people realized there was an important distinction between libre and gratis licenses.

* Prior to the collection split, everyone was in our CoC as they were in our repo.  Why can't we keep it that way?
  * It feels very similar to the question of licensing... prior to the split, we licensed all code under the GPLv3+ and BSD-2-clause but now we've given people power over their own sections of the project so they have the power to choose different licenses, CoC, etc.
  * I think the open source tradeoff applies here: you don't directly pay for all the work being done but in return you have to give up some power to other people in the project.

* Regular test exercises can be helpful
  * From misc: In wikipedia, we did that for a wikipedia user group, and we learned a lot
    * Make a report as if a CoC violation actually happened
    * See who does what, what people forgot, etc
    * Use something with a clear violation as asking to discuss more complex problem could have been emotionally taxing