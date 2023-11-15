---
date: '2022-06-21T14:26:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:id
cardinality: n/a
requirement: Optional
metadata_profile: v3-0-final
---

The `rioxxterms:id` property **MUST NOT** be used directly in the root of a Rioxx record, but **MAY** be used to add identifiers into the following root properties:

* `rioxxterms:contributor`
* `rioxxterms:creator`
* `rioxxterms:publisher`

Identifiers represented by the `rioxxterms:id` property **MUST** be HTTP(S) URIs.
