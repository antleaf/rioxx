---
creators: ["George Macgregor"]
categories: []
date: 2022-06-23
description: ""
draft: false
tags: []
title: "Rioxx: The Research Outputs Metadata Schema v3.0 Release Candidate 1 published"
topics: []
aliases:
---

The [Rioxx Governance Group (RGG)](https://www.rioxx.net/governance/) is pleased to announce the [publication of the v3.0 Release Candidat 1 of Rioxx: The Research Outputs Metadata Schema](https://www.rioxx.net/profiles/v3-0-rc-1/) -- formerly known as the *RIOXX Metadata Application Profile*.

Since July 2021, when the [beta release](https://www.rioxx.net/profiles/v3-0-beta-1/) of v3.0 was made available, the RGG has been working towards incorporating feedback from the repository and scholarly communications communities, and making adjustments to Rioxx to improve the way in which metadata are modelled. The publication of the candidate release today marks the end of this period of consultation but by no means the end -- it will always remain possible for anyone to document issues for future consideration at the [Rioxx GitHub repository](https://github.com/antleaf/rioxx).

I would draw to the attention of readers [the announcement made when the v3.0 beta release was published](https://www.rioxx.net/post/2021/07-06-version-3-0-draft-for-public-comment/), as it provides a useful summary of some of the principal changes between v2.0 and v3.0. Importantly, the specific changes listed in the beta release remain in the candidate release too, which included some significant changes to the use of `<dc:identifier>` and `<dc:relation>`. But in this candidate release we have made some further significant updates:

## Separation of project and grant data
The conflation of project and grant data has been a common problem across a number of metadata schema. Prior to this candidate release, Rioxx was no exception. Research projects can, and do, operate independently of grant funding. Similarly, not all grants result in the creation of a project. Moreover, some projects can persist for many years and receive multiple grants from multiple different funders; yet, many schema conflate projects and grants and thereby fail to accurately model reality. Greater separation of project and grant data is therefore something we have introduced as part of this candidate release, with the creation of `<rioxxterms:grant>` and the re-scoping of `<rioxxterms:project>`.

## Wider use of persistent identifiers
A more inclusive approach to persistent identification and persistent identifiers (PIDs) across `<rioxxterms:author>`, `<rioxxterms:contributor>`, `<rioxxterms:project>` and `<dc:publisher>` has been introduced to reflect the growing maturity of the PID landscape. The v3.0 beta draft permitted a far narrower number of PID schemes. This has been addressed in the candidate release, with most extant schemes supported.

## Rioxx name change
By now you will have released that the name has changed. As there exist many different repository metadata application profiles, it was not uncommon for the consultation process to elicit feedback from community members stating that the label 'RIOXX' was confusing, or that no-one could remember what the acronym stood for, or that the name of the profile failed to adequately communicate its purpose. Some even suggested that the name should be jettisoned altogether! We decided to keep the name, but we can at least make its full title a little more self-explanatory. We have thus elected to refine the name a little and de-acronymize 'RIOXX', since the acronym itself is no longer meaningful:

* *Rioxx: The Research Outputs Metadata Schema*

The name change helps to communicate the raison d'être of Rioxx: to facilitate the improved harvesting, aggregation and discovery of repository content. This change will be reflected in all future dissemination about Rioxx.

# The future
But, of course, to truly facilitate improvements in harvesting, aggregation and discovery, Rioxx needs to be adopted by repositories. This is easier for some repositories to achieve than others, and easier for some organizational teams than others. Even teams with the technical nous may lack the team capacity to oil the wheels of adoption. The RGG is in discussions with a number of bodies and organizations about the possibility of supporting Rioxx v3.0. The shape of support remains uncertain at this stage but formal endorsement and/or technical support for repositories would be a welcome start. Further updates will be posted here in due course.

George Macgregor, RGG Chair - 2022-06-24




