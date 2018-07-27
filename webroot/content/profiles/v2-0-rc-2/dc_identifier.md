---
date: '2016-03-21T10:00:43+00:00'
draft: false
type: metadata_profile_property
title: dc:identifier
cardinality: Exactly one
requirement: Mandatory
metadata_profile: v2-0-rc-2
---
This field **MUST** contain an HTTP URI which is a persistent identifier for ***the resource***. The purpose of this field is, throught direct identification of ***the resource***, to allow access to it, therefore it is **RECOMMENDED** that this identifier should point to the *actual resource being described by the RIOXX record* (typically a file in MS Word or PDF format), rather than to an intermediary resource such as a repository web page. Note that RIOXX does not require any require particular file format to be used for ***the resource***.

To describe another version of ***the resource*** with a different identifier, a completely separate RIOXX record should be created.
