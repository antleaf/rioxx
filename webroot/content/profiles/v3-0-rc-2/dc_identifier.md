---
date: '2023-05-06T10:21:43+00:00'
draft: false
type: metadata_profile_property
title: dc:identifier
cardinality: Exactly one
requirement: Mandatory
metadata_profile: v3-0-rc-2
---
`dc:identifier` **MUST** contain an HTTP(S) URI which is an identifier for *the resource*. In repositories, this is typically a URI which resolves to a repository 'landing page' which may contain links to other related resources. 

It is **RECOMMENDED** that a DOI, Handle.net, OAI ID, URN, or other "persistent" identifier be used in `dc:identifier`. However, a direct repository URI **MAY** be used instead.
