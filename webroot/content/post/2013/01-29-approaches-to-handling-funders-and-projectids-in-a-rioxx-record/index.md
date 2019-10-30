---
title: Approaches to handling funders and projectIDs in a RIOXX record
date: 2013-01-29T00:00:00+00:00
description: 
draft: false
tags: []
topics: []
categories: []
creators: ["Paul Walk"]
aliases:
- "/2013/01/29/Approaches-to-handling-funders-and-projectIDs-in-a-RIOXX-record/"
---

The most important requirement for RIOXX is to provide a way to collect basic information about how research outputs (especially papers) have been funded. That is to say, we need to collect two types of information for a given paper:

* the funder
* the project or grant ID under which this research output was funded

RIOXX has at its heart a simple application profile of Dublin Core, the better to fit naturally with existing technical infrastructure and to be easily implemented. Following from this, it seems that there are the following possibilities for representing funder and projectID in a single record:

![Funder and project id options](/post/2013/01-29-approaches-to-handling-funders-and-projectids-in-a-rioxx-record/funder-and-project_id-options.png)

## Option 1: Separate fields for Funder and ProjectID

This is the ***currently proposed*** approach. It has the virtue of introducing a very low barrier to data collection (the common repository interfaces support this) and provides for the primary use-case which is the collection of funding information about research outputs. In data-modelling terms, this is not a satisfying approach because it is not possible to relate a funder to a project ID within any given record. However:

* it should be possible to build this relationship, if required, after the data has been harvested, using other correlating  information (this is a trade-off for the requirement to implement this in existing platforms and workflows very soon)
* the expression of this relationship is not a requirement in the usecase we are addressing

## Option 2: Separate fields for Funder and ProjectID, ordering is significant

This is ***not a viable*** option as data transfer using XML does not reliably support the ordering of values within multi-value fields.

## Option 3: Composite field for Funder and ProjectID

This is an obvious choice for an approach which does not depend on any extra external development (for example of a global unique ID system for projects/grants). However, this approach could be disruptive to the interfaces and workflows faced by repository managers, and we are aiming for minimal disruption to repository managers who are, after all, a key stake-holder. This option is still open for discussion and, indeed, we are discussing this with developers from the ePrints and DSpace communities.

## Option 4: Syntactically rich string containing Funder and ProjectID components

This approach concatenates funder and projectID into one string, using an agreed delimiter character to separate them. This is the approach used in the OpenAIRE guidelines, and one which we have considered closely. We have decided to reject this approach because the projectIDs we will need to accommodate are unpredictable, and liable to contain whatever character we use to delimit this string. There are approaches to mitigating this issue - notably using encoding approaches such as URLEncoding - but this places an extra processing burden on suppliers and consumers with no guarantee that this will be implemented - this approach is therefore considered non-optimal and 'fragile'.

## Option 5: Globally unique projectID

This is a more aspirational option - it cannot be implemented in the short-term because a system of globally uniques and persistent identifiers for grant-funded projects does not yet exist. However, in the medium-term this is feasible and is something we hope to explore in a later phase.

## Next steps

We are now working with experts from the ePrints and DSpace communities to figure out what is viable in the short term. Our default position is to implement *option 1*. If we can implement *option 3* without damaging the chances of the overall solution being adopted by repository managers on the common platforms, then this would be an attractive solution for the short term. For the longer term, we will continue to consider approaches to *option 5* or, better still, a combination of *option 5* and *option 1*, where the funders are also listed separately to the projectID (and actionable and persistent identifier which points to metadata about the funder), simply to avoid the need for multiple round-trip queries to, for example, list records with a given funder.

Comments on all/any aspects of this are welcome!


<!-- ----

#### Comments

##### Comment by [Pablo de Castro](http://www.repositorynet.ac.uk/) on 2013/01/30 at 11:13

Hi Paul,

I fully agree with the RIOXX conclusion of selecting Option 1 as the default one and checking out whether Option 3 (which would certainly provide far more accurate metadata) is technically and socially feasible. While steps are simultaneously being taken to provide the [FundRef](http://www.crossref.org/fundref/index.html)/GrantDOI system which will eventually enable Option 5, it might be useful as well to pay attention to this rather old proposal from funders in this regard – namely to feature some kind of standardised funder code within the ProjectID (Option 4) that will uniquely identify the funding agency for a given project. OpenAIRE guidelines do naturally take a simple approach to this, since it’s mainly EU FP7-funded projects they’re dealing with, but major UK funders have already agreed a two- or three-letter code that will provide default funder identification for a given project (there should be a publicly available code list somewhere I presume?) The issue with this is of course that it was quite recently implemented and will therefore not be providing a solution for older projectIDs. But it would be useful anyway to keep track of initiatives aiming to provide automatic links between grantIDs and corresponding funders (including of course the one-to-many use case).
Thanks, Pablo

----

##### Comment by Anna Clements on 2013/02/12 at 17:03

Paul – can we go for 3 …or at least allow both 1 and 3 from the outset; those of us with CRIS system can do 3 straight off and it would seem sensible to allow for that from the outset.

----
 -->