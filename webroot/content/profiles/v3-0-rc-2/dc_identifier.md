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

<mark>I'm not sure we should be putting `rel` attributes into metadata properties like this (below)? Signposting isn't being used here... (Paul)</mark>

<s>
`dc:identifier` can be modified by the `rel` attribute. The `rel` attribute is based on the [Signposting](https://signposting.org/) notion of ['publication boundaries'](https://signposting.org/publication_boundary/). This attribute can be helpful to machines and in most Rioxx cases **SHOULD** be set to `collection`.

<mark>QUESTION: Are there scenarios where it might be set to `item`?</mark>
</s>