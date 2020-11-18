---
date: '2020-11-18T14:00:43+00:00'
draft: false
type: metadata_profile_property
title: dc:relation
cardinality: Zero or more
requirement: Optional
metadata_profile: v3-0-draft
---
The format of this element **MUST** be an HTTP URI which points to a related resource, e.g. a research dataset which underpins ***the resource***. An exception to this is the DOI identifying the related 'version of record' - this **MUST** be recorded in the *rioxxterms:version_of_record* element.

Each related resource **MUST** appear as a separate instance of the field.
