---
date: '2021-01-15T14:00:43+00:00'
draft: false
type: metadata_profile_property
title: dc:relation
cardinality: Zero or more
requirement: Optional
metadata_profile: v3-0-draft
---

(Note that the related 'version of record' is not recorded here but **MUST** be recorded in the *rioxxterms:version_of_record* element.)

The *resource* described by a RIOXX record is commonly a web page containing metadata and links to other resources, such as (in the case of a publication) a PDF file. The `dc:relation` property identifies these other, related resources. Each `dc:relation` property **MUST** contain an HTTP(S) URI, and **MUST** include the following attributes: 

* `type`
* `deposit_date`

The `type` attribute must contain a value which is an identifier from the schema.org vocabulary. For example, for a







Each related resource **MUST** appear as a separate instance of the element.
