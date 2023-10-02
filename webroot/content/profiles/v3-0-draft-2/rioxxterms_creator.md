---
date: '2022-06-21T14:26:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:creator
cardinality: One or more
requirement: Mandatory
metadata_profile: v3-0-draft-2
---

This property describes the party responsible for creating *the resource*. This is normally a person, but may be an organisation or service.

Where available and possible, the **RECOMMENDED** format is to add the name of the creator as the content of the property, and to include a recognised identifier in its HTTP(S) URI form using a child `rioxxterms:id` property, e.g.

```xml
<rioxxterms:creator>
    <rioxxterms:name>Smith, Adam</rioxxterms:name>
    <rioxxterms:id>https://isni.org/isni/0000000122796642</rioxxterms:id>
</rioxxterms:creator>
```

If necessary, multiple instances of `rioxxterms:id` may be included to communicate additional identifier schemes, e.g.

```xml
<rioxxterms:creator>
    <rioxxterms:name>Fry, Hannah</rioxxterms:name>
    <rioxxterms:id>https://isni.org/isni/0000000446254946</rioxxterms:id>
    <rioxxterms:id>http://viaf.org/viaf/314908506</rioxxterms:id>
    <rioxxterms:id>https://orcid.org/0000-0003-0601-9100</rioxxterms:id>
</rioxxterms:creator>
```

Where an organisation requires attribution, the **RECOMMENDED** format is to add the official name of the organisation as the content of `rioxxterms:creator`, and to include a recognised persistent identifier scheme in its HTTP(S) URI form within `rioxxterms:id`. Such an identifier scheme might include [ISNI](https://isni.org), [Research Organization Registry](https://ror.org/), [VIAF](http://viaf.org/) or [WikiData concept URI](https://www.wikidata.org/), e.g.

```xml
<rioxxterms:creator>
    <rioxxterms:name>C.E.R.N.</rioxxterms:name>
    <rioxxterms:id>https://isni.org/isni/000000012156142X</rioxxterms:id>
    <rioxxterms:id>https://ror.org/01ggx4157</rioxxterms:id>
</rioxxterms:creator>
```

Where the `rioxxterms:creator` property appears multiple times for one record, it **CAN** be assumed that the order is significant, in that the first element describes the first named author of *the resource*. In order to make this more explicit, an extra attribute, `first-named-author`, **SHOULD** be used to indicate which of the `rioxxterms:creator` elements describes the first named author of *the resource*, thus:

```xml
<rioxxterms:creator first-named-author="true">
    <rioxxterms:name>Olusoga, David</rioxxterms:name>
    <rioxxterms:id>https://isni.org/isni/0000000096386112</rioxxterms:id>
</rioxxterms:creator>
```





