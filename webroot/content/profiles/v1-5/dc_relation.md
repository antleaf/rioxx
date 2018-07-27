---
date: '2016-03-21T10:00:43+00:00'
draft: false
type: metadata_profile_property
title: dc:relation
cardinality: Zero or more
requirement: Optional
metadata_profile: v1-5
---
The format of this element **SHOULD** be an HTTP URI which points to a related resource, e.g. a data-set which underpins ***the resource***. An exception to this is the DOI identifying a related 'version of record' - this should be recorded in the *rioxxterms:version_of_record* element.

Each related resource **MUST** appear as a separate instance of the field.
