---
date: '2020-11-18T13:00:43+00:00'
draft: false
type: metadata_profile_property
title: dc:publisher
cardinality: Zero or more
requirement: Recommended
metadata_profile: v3-0-draft
---

This element contains the name of the entity, typically a &#39;publisher&#39;, responsible for making the ***version of record*** of ***the resource*** available. This could be a person, organisation or service.

Where available and possible, the **RECOMMENDED** format is to add the official name of the publisher, and to include an [ISNI](http://isni.org) ID, if known, in its HTTP(S) URI form, e.g.

```xml
<dc:publisher uri="https://isni.org/isni/000000040482455X">
    Public Library of Science
</dc:publisher>
```

Where an ISNI is unavailable or cannot be provided, the name of the publisher entered here **SHOULD** instead be from a controlled list.
