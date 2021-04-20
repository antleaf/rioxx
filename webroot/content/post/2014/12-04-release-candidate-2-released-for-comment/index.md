---
title: Release Candidate 2 Released For Comment
date: 2014-12-04T09:34:55+00:00
description: 
draft: false
tags: []
topics: []
categories: []
creators: ["Paul Walk"]
aliases:
- "/2014/12/04/Release-Candidate-2-Released-For-Comment/"
---

Following further public consultation and discussion with stakeholders, we have just released  [RIOXX 2.0 Release Candidate 2](/v2-0-rc-2) for comment.

The changes from RIOXX 2.0 Beta 1 are detailed in the [release notes](/release_notes/), but the most significant change is that we have added a recommendation to use [ISNI](http://isni.org) identifiers for for organisations when named as authors, contributors or funders.

We think RIOXX 2.0 is very close to being ready for its final release and are aiming for a release date of 2015-01-09.

## NISO's Access and License Indicators guidelines
RIOXX is required, following Jisc's [V4OA process](http://www.webarchive.org.uk/wayback/archive/20140701123059/http://v4oa.net/), to use two properties from the NISO's [Access and License Indicators](http://www.niso.org/workrooms/ali/) guidelines: 'license_ref' and 'free_to_read'. While the guidelines are still in a final review process, we have been assured that there will be no significant changes to these.

The 'license_ref' property is the most important of these - it's *mandatory* in a RIOXX record, while 'free_to_read' is optional.

## The license_ref property
This property, which is mandatory for a RIOXX record requires an HTTP URI and a date, where the HTTP URI identifies a particular license. The ideal case is the use of one of the licenses which are acceptable to RCUK & HEFCE, such as [http://creativecommons.org/licenses/by/4.0](http://creativecommons.org/licenses/by/4.0).

It is recognised that there will, however, be cases where either the license is not known, or where no appropriate HTTP URI has been established to identify the license.  We did contemplate making 'license_ref' an *optional* property, but decided against this, on the grounds that this would undermine the drive towards clearer licensing of open access materials. Instead, we have taken steps which maintain the integrity of the mechanism supported by the use of the 'license_ref' property, while allowing repository managers to supply information in a valid RIOXX record.

The absence of a license means that the default copyright position of "All Rights Reserved" applies. For convenience, we have 'minted' the HTTP URI '[http://www.rioxx.net/licenses/all-rights-reserved](http://www.rioxx.net/licenses/all-rights-reserved)' for such situations.

A particular, common case for repositories will be where an item is held in the repository under *embargo*. In such cases, the item is not licensed for use, and the default copyright position of "All Rights Reserved" applies. Again, for convenience, we have minted an HTTP URI, '[http://www.rioxx.net/licenses/under-embargo-all-rights-reserved](http://www.rioxx.net/licenses/under-embargo-all-rights-reserved)', for embargoed items.

In neither of these cases are we creating some new license expression, but we are allowing the mechanism which requires explicit URIs to function, and are making the absence of a license *explicit*, rather than *inferred*.

Beyond this, the license entered here will be that demanded by the funder, the publisher or the owner of the repository (or even the author), depending on the circumstances (e.g. green/gold).

We welcome comment (please use the comments facility on this blog) on this, or on any aspect of RIOXX 2.0 RC 2.

***Edit**: this post has been slightly edited to make clear that the recommendation to use ISNI to identify authors and contributors applies only where the author or contributor is an organisation rather than a person. ORCID remains the recommended identifier scheme for individual people.*