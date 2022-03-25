---
date: '2020-10-09T14:00:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:type
cardinality: One or more
requirement: Mandatory
metadata_profile: v3-0-draft
---
Type refers to the 'type' - the nature or genre of the content of ***the resource***. This element should not be confused this with `dc:format`.

Values recorded at `rioxxterms:type` **MUST** be taken from the [COAR Controlled Vocabulary for Resource Type Genres](http://vocabularies.coar-repositories.org/documentation/resource_types/) (Version 2.0), which provides a hierarchical model of resource type genres supported by language independent HTTP(S) URIs.

Example:

```xml
<rioxxterms:type uri="https://purl.org/coar/resource_type/c_5794">
    conference paper
</rioxxterms:type>
```



The COAR Controlled Vocabulary for Resource Type Genres is detailed in its treatment of type genres. It is anticipated that only the largest repositories would accommodate all vocabulary values, with most others implementing a subset in line with the resource types managed by the repository.
