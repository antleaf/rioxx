---
title: On validation
date: 2015-05-06T08:27:26+00:00
description: 
draft: false
tags: []
topics: []
categories: []
creators: ["Paul Walk"]
aliases:
- "/2015/05/06/On-validation/"
---

Following a very useful discussion with Mike Taylor (see comments on [this post](/2015/04/23/rioxx-records-in-the-wild/)), I have split the validation of RIOXX records into two stages:

1. a basic syntax check, following less strict rules and constraints than the full RCUK requirements
2. a strict validation check against the full RCUK requirements

The reason for doing this is to allow implementers to check that their software is correctly set-up. For example, if a RIOXX-enabling plugin for a repository is correctly configured, but the repository's metadata holds values for the 'version' which are not from the RCUK-approved vocabulary for versions, then records from that repository will fail the full RCUK validation test. However, it will be useful for repository managers to have some reassurance that at least their repository software, and any RIOXX plugin, are functioning correctly. Hence the second, basic RIOXX validation.

This approach opens up the possibility of further, separate, profiles of RIOXX for other business cases, where the RIOXX syntax (and consequently repository system plugins) need not change.

[View results of testing samples from several repositories for conformance to the two profiles](/implementation).

Kudos to the ['Enlighten' repository at Glasgow University](http://eprints.gla.ac.uk) for being the first repository tested to have passed the basic RIOXX validation test!

I hope this is not confusing - it is intended to help.

Comments welcome!

