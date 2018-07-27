---
categories: []
date: '2016-03-21T10:00:43+00:00'
description: ''
draft: false
tags: []
title: RCUK RIOXX Application Profile Version 1.2a (DEPRECATED)
topics: []
type: metadata_profile_document
metadata_profile_name: v1-2-a
aliases:
- "/v1-2-a/"
---


Note that there is a newer version of the application profile - [please check here for the latest version](http://rioxx.net/versions/)

This is an updated version of the RIOXX applicaiton profile, enhanced following the outcomes of the [V4OA](http://www.v4oa.net) project.

## Changes since version 1.0

* the &lt;free_to_read&gt; element has been added
* the &lt;license_ref&gt; element has been added
* the &lt;dc:rights&gt; element has been removed - the introduction of the new &lt;license_ref&gt; has superceded this
* the recommendations for the &lt;rioxxterms:funder&gt; element have changed - the use of [FundRef](http://www.crossref.org/fundref/) is now recommended.
* the &lt;rioxxterms:apc&gt; element has been added
* the &lt;rioxxterms:version&gt; element has been added
* the &lt;rioxxterms:creator&gt; element has been replaced with &lt;rioxxterms:author&gt;
* the &lt;rioxxterms:funder&gt; element now has an *id* attribute
* the &lt;rioxxterms:version-of-record&gt; element has been added

***Note that we may introduce a controlled voicabulary of output types into this version, if RCUK can supply an authoritative list. This would then constrain the values of the &lt;dc:rights&gt; element***


This section details the application profile for RIOXX. The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC 2119](http://www.ietf.org/rfc/rfc2119.txt).
