---
date: '2020-12-04T10:21:43+00:00'
draft: false
type: metadata_profile_property
title: dc:identifier
cardinality: Exactly one
requirement: Mandatory
metadata_profile: v3-0-draft
---
This field **MUST** contain an HTTP(S) URI which is a persistent identifier for ***the resource***. The purpose of this field is, through direct identification of ***the resource***, to allow access to it, therefore it is **RECOMMENDED** that this identifier should point to the *actual resource being described by the RIOXX record* (typically a file in MS Word or PDF format), rather than to an intermediary resource such as a repository web page. 

Note that RIOXX does not require any require particular file format to be used for ***the resource***.

To describe another version of ***the resource*** with a different identifier, a completely separate RIOXX record should be created.

@@@Need for dcterms:hasFormat to accommodate different 'expressions' of a PDF, e.g. JATS, Word, etc. 