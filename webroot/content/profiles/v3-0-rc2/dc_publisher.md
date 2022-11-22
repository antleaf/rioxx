---
date: '2022-11-22T11:00:43+00:00'
draft: false
type: metadata_profile_property
title: dc:publisher
cardinality: Zero or more
requirement: Recommended
metadata_profile: v3-0-rc-2
---

This property contains the name of the entity, typically a &#39;publisher&#39;, responsible for making the ***version of record*** of ***the resource*** available. This could be a person, organisation or service.

Where available and possible, the **RECOMMENDED** format is to add the official name of the publisher, and to include a recognised persistent identifier in its HTTP(S) URI form as an attribute, e.g.

```xml
<dc:publisher uri="https://isni.org/isni/000000040482455X">
    Public Library of Science
</dc:publisher>
```

```xml
<dc:publisher uri="https://ror.org/00qpqrv96">
    Ubiquity Press (United Kingdom)
</dc:publisher>
```

Typical persistent identifier schemes likely to be relevant here include [ISNI](https://isni.org/), [ROR](https://ror.org/), [GRID](https://www.grid.ac/), [VIAF](http://viaf.org/). Where a recognised persistent identifier is unavailable or cannot be provided, the name of the publisher entered here **SHOULD** instead be from a controlled list.

Systems wishing to communicate the existece of multiple URIs for a single publisher **SHOULD** repeat `dc:publisher`. For example, a system wishing to expose both an ISNI and ROR ID in relation to a single resource should represent the data as follows:

```xml
<dc:publisher uri="https://isni.org/isni/000000040482455X">
    Public Library of Science
</dc:publisher>
<dc:publisher uri="https://ror.org/03bdvdc06">
    Public Library of Science
</dc:publisher>
```
