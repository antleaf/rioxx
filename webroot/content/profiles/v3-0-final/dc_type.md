---
date: '2023-10-20T14:00:43+00:00'
draft: false
type: metadata_profile_property
title: dc:type
cardinality: One or more
requirement: Mandatory
metadata_profile: v3-0-final
---

Type refers to the nature or genre of the content of *the resource*. This property should not be confused with the `type` attribute in `dc:relation`.

The value recorded in `dc:type` **MUST** be an HTTP(S) URI taken from the [COAR Controlled Vocabulary for Resource Type Genres](http://vocabularies.coar-repositories.org/documentation/resource_types/), which provides a hierarchical model of resource type genres.

<!-- @g3om4c - Do we want to soften the requirement for COAR vocabulary to include others, such as schema.org -- or even nod to the ability to relate this property to include both? -->

Example:

```xml
<dc:type>
    https://purl.org/coar/resource_type/c_5794
</dc:type>
```
