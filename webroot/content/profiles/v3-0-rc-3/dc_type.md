---
date: '2023-06-02T14:00:43+00:00'
draft: false
type: metadata_profile_property
title: dc:type
cardinality: One or more
requirement: Mandatory
metadata_profile: v3-0-rc-3
---

Type refers to the nature or genre of the content of *the resource*. This property should not be confused with `dc:format`.

The value recorded in `dc:type` **MUST** be an HTTP(S) URI taken from the [COAR Controlled Vocabulary for Resource Type Genres](http://vocabularies.coar-repositories.org/documentation/resource_types/), which provides a hierarchical model of resource type genres.

Example:

```xml
<dc:type>
    https://purl.org/coar/resource_type/c_5794
</dc:type>
```
