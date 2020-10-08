---
date: '2016-03-21T10:00:43+00:00'
draft: false
type: metadata_profile_property
title: dc:relation
cardinality: Zero or more
requirement: Optional
metadata_profile: v2-0-final
---
The format of this element **MUST** be an HTTP URI which points to a related resource, e.g. a research data-set which underpins ***the resource***. An exception to this is the DOI identifying the related 'version of record' - this **MUST** be recorded in the *rioxxterms:version_of_record* element.

Each related resource **MUST** appear as a separate instance of the field.
