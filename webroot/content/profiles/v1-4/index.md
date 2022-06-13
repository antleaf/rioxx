---
categories: []
date: '2016-03-21T10:00:43+00:00'
description: ''
draft: false
tags: []
title: RCUK RIOXX Application Profile Version 1.4
topics: []
aliases:
- "/v1-4/"
status: obsolete
---obsolete

This is an updated version of the RIOXX application profile, enhanced following the outcomes of the [V4OA](http://www.v4oa.net) project.

## Changes since version 1.0

* the <free_to_read> element has been added
* the <license_ref> element has been added
* the <dc:rights> element has been removed - the introduction of the new <license_ref> has superceded this
* the recommendations for the <rioxxterms:funder> element have changed - the use of [FundRef](http://www.crossref.org/fundref/) is now recommended.
* the <rioxxterms:apc> element has been added
* the <rioxxterms:version> element has been added
* the <rioxxterms:creator> element has been replaced with <rioxxterms:author>
* the new <rioxxterms:project> element has replaced both <rioxxterms:projectid> and <rioxxterms:funder>
* the <rioxxterms:version-of-record> element has been added, and the recommendation to include, under <dc:relation>, the DOI to the version of record has been removed.
* the <dcterms:issued> element has been replaced with the <rioxxterms:acceptdate> and the meaning of this element has changed.

## Terminology

***the resource*** refers to the electronic copy of an article held in a repository, and is the thing being described by the RIOXX metadata record.

***version of record*** refers to the instance of the article being described in the RIOXX metadata record which has been made available, electronically, by the publisher.

The terms **MUST**, **MUST NOT**, **REQUIRED**, **SHALL**, **SHALL NOT**, **SHOULD**, **SHOULD NOT**, **RECOMMENDED**, **MAY**, and **OPTIONAL** used in the table below should be interpreted as described in [RFC 2119](http://www.ietf.org/rfc/rfc2119.txt).
