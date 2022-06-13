---
date: '2016-03-21T10:00:43+00:00'
draft: false
type: metadata_profile_property
title: dc:identifier
cardinality: Exactly one
requirement: Mandatory
metadata_profile: v1-5
---
This field **MUST** contain a globally unique and persistent identifier for ***the resource***. The identifier **SHOULD** be an HTTP URI that can be de-referenced (and is, thus, &#34;actionable&#34;). The purpose of this field is to allow access to ***the resource***, therefore it is **RECOMMENDED** that this identifier should point to the *actual resource being described by the RIOXX record* (typically a file in MS Word format), rather than to an intermediary resource such as a repository web page.

To describe another version of ***the resource*** with a different identifier, a completely separate RIOXX record should be created.
