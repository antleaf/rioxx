---
date: '2023-06-02T14:00:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:type
cardinality: One or more
requirement: Mandatory
metadata_profile: v3-0-rc-2
---

<mark>this is a little confusing - better to simply require the URI as value?</mark>
Type refers to the nature or genre of the content of *the resource*. This property should not be confused with `dc:format`.

The human readable value recorded in `rioxxterms:type` **MUST** be taken from the [COAR Controlled Vocabulary for Resource Type Genres](http://vocabularies.coar-repositories.org/documentation/resource_types/), which provides a hierarchical model of resource type genres. This is supported by language independent HTTP(S) URIs, encoded within the `coar_type` attribute.

Example:

```xml
<rioxxterms:type coar_type="https://purl.org/coar/resource_type/c_5794">
    conference paper
</rioxxterms:type>
```

<mark>Next para seems redundant</mark>
~~The COAR Controlled Vocabulary for Resource Type Genres is detailed in its treatment of type genres. It is anticipated that only the largest repositories would accommodate all vocabulary values, with most others implementing a subset in line with the resource types managed by the repository.~~

