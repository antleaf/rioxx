---
date: '2022-11-22T11:00:43+00:00'
draft: false
type: metadata_profile_property
title: "rioxxterms:publisher"
cardinality: Zero or more
requirement: Recommended
metadata_profile: v3-0-rc-2
---

<mark>
I have changed the name to `rioxxterms:publisher` and used the child `rioxxterms:id` approach instead of an attribute. This is now consistent with `rioxxterm:author` and `rioxxterms:contributor`. (Paul)
</mark>


This property contains the name of the entity, typically a publisher, responsible for making the *version of record* of *the resource* available. This could be a person, organisation or service.


Where available and possible, the **RECOMMENDED** format is to add the official name of the publisher as the content of the property, and to include a recognised identifier in its HTTP(S) URI form using a child `rioxxterms:id` property, e.g.
```xml
<rioxxterms:publisher>
    Public Library of Science
    <rioxxterms:id>https://isni.org/isni/000000040482455X</rioxxterms:id>
</rioxxterms:publisher>
```

```xml
<rioxxterms:publisher>
    Ubiquity Press (United Kingdom)
    <rioxxterms:id>https://ror.org/00qpqrv96</rioxxterms:id>
</rioxxterms:publisher>
```

Typical identifier schemes likely to be relevant here include [ISNI](https://isni.org/), [ROR](https://ror.org/), and [VIAF](http://viaf.org/). Where a recognised identifier is unavailable or cannot be provided, the name of the publisher entered here **SHOULD** instead be from a controlled list.<mark>QUESTION: which controlled list(s)? Is this useful??</mark>

Systems wishing to communicate the existence of multiple URIs for a single publisher may repeat `rioxxterms:publisher`.