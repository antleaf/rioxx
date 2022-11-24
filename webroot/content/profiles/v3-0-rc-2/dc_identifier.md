---
date: '2022-03-31T10:21:43+00:00'
draft: false
type: metadata_profile_property
title: dc:identifier
cardinality: Exactly one
requirement: Mandatory
metadata_profile: v3-0-rc-2
---
`dc:identifier` **MUST** contain an HTTP(S) URI which is a persistent identifier for ***the resource***. In repositories, this is typically a webpage which includes links to other related resources. It is **RECOMMENDED** that that a DOI, Handle, URN, or other persistent identification scheme be used. In the common case of a "splash-page" linking to related files (potentially in different formats), then one or more instances of the `dc:relation` property may be included in the Rioxx record to convey this and thereby direct harvesting software agents.

Note that `dc:identifier` should not be confused with `rioxxterms:version_of_record`.
