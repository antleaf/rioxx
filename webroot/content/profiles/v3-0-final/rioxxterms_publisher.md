---
date: '2022-11-22T11:00:43+00:00'
draft: false
type: metadata_profile_property
title: "rioxxterms:publisher"
cardinality: Zero or more
requirement: Recommended
metadata_profile: v3-0-final
---

This property contains the name of the entity, typically a publisher, responsible for making the *version of record* of *the resource* available. This could be a person, organisation or service.


Where available and possible, the **RECOMMENDED** format is to add the official name of the publisher as the content of the property, and to include one or more recognised identifiers in their HTTP(S) URI form using child `rioxxterms:id` properties, e.g.
```xml
<rioxxterms:publisher>
    <rioxxterms:name>Public Library of Science</rioxxterms:name>
    <rioxxterms:id>https://isni.org/isni/000000040482455X</rioxxterms:id>
    <rioxxterms:id>https://isni.org/isni/0000000404826432</rioxxterms:id>
</rioxxterms:publisher>
```

```xml
<rioxxterms:publisher>
    <rioxxterms:name>Ubiquity Press (United Kingdom)</rioxxterms:name>
    <rioxxterms:id>https://ror.org/00qpqrv96</rioxxterms:id>
</rioxxterms:publisher>
```

Typical identifier schemes likely to be relevant here include [ISNI](https://isni.org/), [ROR](https://ror.org/), and [VIAF](http://viaf.org/). 
