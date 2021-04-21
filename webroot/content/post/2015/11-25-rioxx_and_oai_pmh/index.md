---
categories: []
date: 2015-11-25T13:21:41Z
description: ""
draft: false
tags: []
title: RIOXX and OAI PMH
topics: []
creators: ["Paul Walk"]
aliases:
- "/2015/11/25/RIOXX-and-OAI-PMH/"
---

Currently, all of those institutional repositories which have declared support for RIOXX are based on the ePrints software, using a plugin especially developed to support RIOXX. There is a little (although not much) information about this plugin [here](https://www.jisc.ac.uk/repository-technical-support) - Jisc paid for the work, but it is not clear from that page who actually did the development (although there is a useful list of potential sources of technical support).

A manager of one of these repositories recently contacted me to suggest that  the validation and reporting script (output [here](http://www.rioxx.net/implementation/)) was offering a distorted view of the adoptions and accuracy or RIOXX reporting because it was harvesting a sample of the *first 10 records*, rather than harvesting more recently created or updated records which had more chance of being RIOXX-compatible.

There is a reason why this should not actually make any difference - and I'll come on to that in a moment- but in the meantime, we have re-run the script, configuring the OAI-PMH request to only ask for records with a date-stamp since 2015-01-01 (as well as a metadata-format of 'rioxx'). Formally, the OAI-PMH request therefore becomes:

<pre><code class="language-http">{BASE-URLl}?verb=ListRecords&from=2015-01-01&metadataPrefix=rioxx</code></pre>

where {BASE-URL} is the *base URL* of a given repository.

The results of this are somewhat different to the results from previously, where we did not specify any date-stamp. What this suggests is that the OAI-PMH request which *ought* to work:

<pre><code class="language-http">{BASE-URL}?verb=ListRecords&metadataPrefix=rioxx</code></pre>


is actually returning records which the repository managers might not wish it to be returning - that is to say records which are not actually ready to be declared as 'RIOXX-compatible'. The OAI-PMH standard [states that](http://www.openarchives.org/OAI/openarchivesprotocol.html#ListRecords):

> Records should be included only for items from which the metadata format
matching the metadataPrefix can be disseminated.

I have no idea if this is a fault in the ePrints plugin, or if it is more to do with the way in which it has been configured. It ought to be something which can be fixed though, so I wonder if any repository managers - particularly those who have implemented the ePrints plugin - have any views on this? Now that there has been some time to work with this plugin, there may be emerging good practice in terms of its configuration and deployment worth sharing with peers.

It may be that we can improve on those compliance rates by simply filtering what are being disseminated as 'RIOXX-compatible' records.

In the spirit of open collaboration, please feel free to leave comments below!