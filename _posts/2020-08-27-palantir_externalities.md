---
layout: post
title:  "Palantir as Keystone XL"
date:   2020-08-27
---

*Epistemic status: Low confidence, written to work through this for myself*

The release of [Palantir's S-1][palantir_s1] has revived discussion about the ethics of its business and its ongoing work for government agencies that many see as perpetrating injustice.

Byrne Hobart has a relatively solid, brief treatment [here][hobart_palantir] that covers the business and political (and cult?) angles, highlighting that:

>"The question from Palantir’s perspective is, once a policy is decided, whether it should be implemented well or poorly; should US counterterrorism involve ad hoc, poorly-coordinated privacy violations, or should the data the government already collects be collated into some usable form so the actual threats can be identified and mitigated?"

To me, this feels just a hair too simplistic, in that it elides the iterative / temporal nature of policy-making around new technology. In this case, perhaps surprisingly, I think the controversy around crude oil transport out of western Canada is illustrative.

For oil sands producers in Alberta, there are effectively [2 ways][wcs_discount] to get their product to market, via rail or via pipeline.

Rail shipments are more spill-prone and less efficient (more expensive), but run on existing rights of way and so don't (generally) require incremental political / public approval to increase shipments (though rail cars have been a constraint in recent years). This maps to existing surveillance methods potentially supplanted by tools like Palantir's, methods which don't make full use of the data being collected due to the cost and inefficiency of manual analysis (and the constraints on hiring enough analysts).

Pipelines, on the other hand, are less prone to spills and more efficient (less expensive) for a given volume of oil transported, but usually involve some incremental land disturbance. The oil is being produced already, and in [increasing volumes][historical_production], just at a [steep discount][wcs_discount] to Gulf Coast prices due to the difficulties of getting it to market.

The tradeoff between the value of oil to civilization and the damage from oil spills in transit is reduced through the technology of pipelines. As Byrne puts it: "Technology is all about escaping those dichotomies: getting more outputs from the same input".

But, because pipelines are linear assets that cross many political jurisdictions, they can be disproportionately impacted by political pressure or the actions of individual stakeholder groups (despite being more efficient / less spill-prone). Yet one could argue that oil is foundational to modern civilization, and so its transport to market should be as clean and efficient as possible and not be subject to the whims of individual stakeholders.

To crib Byrne's framing above: "Should oil shipment involve inefficient, spill-prone rail that is capacity constrained, or should we use pipelines to ship oil (that's already being produced) more cheaply and cleanly?"

This is the same type of technology solution that Palantir is purportedly selling; security is foundational to modern civilization and so one could argue that its provision should be as effective and efficient (minimally invasive / rights infringing) as possible, and not be subject to the whims of [individual stakeholders][maven_withdrawal].

But in focusing on the elimination of one tradeoff (oils spills vs oil use; privacy invasion vs increased security), this framing glosses over another critical piece of the puzzle: "once a policy has been decided". These decisions are not one-shot, but in fact are part of continuously evolving feedback loops, constrained by the possible, that take **time** to reach their conclusion.

This is doubly important because it is not always a question of achieving output X more efficiently with technology B than technology A, but rather that the deployment of technology B actually results in a higher output Y. The construction of pipelines, and the attendant reduction of oil transport costs, could reasonably be expected to increase the volume of oil produced. If history is any guide, the purported improvements from the use of Palantir's software could increase the volume of data collected and privacy infringed (even if the damage to any given person is much smaller).

It can be argued that the tradeoffs involved in oil and security provision are not immediately, fully accounted for and controlled through the current political / governance process. Unabated oil extraction is rapidly bringing on dangerous climate change; the rapid expansion of the security state has led to [gaps][aclu_xkeyscore] in [democratic][snowden] [oversight][drone_strikes].

This is not to disagree with Byrne's '[compromise through presumed incompetence][compromise]'. We should not settle for inefficient technologies because we can't stomach a political compromise. Yet I can't help but think there is an element of allowing time for that political process to work.

In the decade since the pipeline protests began in Canada, the federal government has implemented a carbon tax to support the transition away from carbon-intensive production and consumption. It has also bought a key pipeline to try to enable the expansion of exports to the coast. Since the Snowden leaks, among others, democratically-elected representatives in the US have been pressured to at least gesture toward better management of government security and surveillance efforts.

This argument is pragmatic rather than categorical; there is no coherent way to say we should do bad things more slowly without potentially slowing down good advancements, since 'bad' and 'good' are politically determined. But it may not always be "[morally lazy][hobart_palantir]" to ask that such democratically-determined control measures are in place **before** the technologies in question are deployed widely.

[palantir_s1]: [https://www.sec.gov/Archives/edgar/data/1321655/000119312520230013/d904406ds1.htm]

[hobart_palantir]: [https://diff.substack.com/p/palantir-on-business-cults-and-politics]

[historical_production]: [https://www.cer-rec.gc.ca/nrg/sttstc/crdlndptrlmprdct/stt/crdlsmmr/crdlsmmr-eng.html]

[wcs_discount]: [https://www.oilsandsmagazine.com/market-insights/crude-oil-pricing-differentials-why-alberta-crude-sells-at-deep-discount-to-wti]

[maven_withdrawal]: [https://www.wired.com/story/google-wont-renew-controversial-pentagon-ai-project/]

[aclu_xkeyscore]: [https://www.aclu.org/blog/national-security/secrecy/guide-what-we-now-know-about-nsas-dragnet-searches-your]

[snowden]: [https://www.bbc.com/news/world-us-canada-23123964]

[drone_strikes]: [https://web.law.columbia.edu/human-rights-institute/counterterrorism/drone-strikes/counting-drone-strike-deaths]

[compromise]: [https://diff.substack.com/p/against-compromise-through-presumed]
