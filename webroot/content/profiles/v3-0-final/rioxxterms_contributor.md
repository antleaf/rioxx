---
date: '2023-11-28T14:58:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:contributor
cardinality: Zero or more
requirement: Optional
metadata_profile: v3-0-final
---

The `rioxxterms:contributor` property describes the party responsible for making contributions to the content of *the primary resource*. This is normally a person, but may be an organisation or service.

Where available and possible, the **RECOMMENDED** format is to encode the name of the contributor within the sub-property `rioxxterms:name`, and to include a recognised identifier in its HTTP(S) URI form using the `rioxxterms:id` sub-property, e.g.

```xml
<rioxxterms:contributor>
	<rioxxterms:name>Bhopal, Kalwant</rioxxterms:name>
	<rioxxterms:id>https://orcid.org/0000-0003-3017-6595</rioxxterms:id>
</rioxxterms:contributor>
```

If necessary, multiple instances of `rioxxterms:id` may be included to communicate additional identifier schemes, e.g.

```xml
<rioxxterms:contributor>
	<rioxxterms:name>Bhopal, Kalwant</rioxxterms:name>
	<rioxxterms:id>https://orcid.org/0000-0003-3017-6595</rioxxterms:id>
	<rioxxterms:id>https://isni.org/isni/0000000038079210</rioxxterms:id>
	<rioxxterms:id>https://www.wikidata.org/wiki/Q61998297</rioxxterms:id>
</rioxxterms:contributor>
```
Where the contributor is an organisation, the **RECOMMENDED** format is to add the official name of the organisation as the content of `rioxxterms:contributor` and to include a recognised persistent identifier scheme in its HTTP(S) URI form within an instance of `rioxxterms:id`. Such an identifier scheme might include [ISNI](https://isni.org), [Research Organization Registry](https://ror.org/), [VIAF](http://viaf.org/) or [WikiData concept URI](https://www.wikidata.org/), e.g.

```xml
<rioxxterms:contributor>
	<rioxxterms:name>Stanford University</rioxxterms:name>
	<rioxxterms:id>https://isni.org/isni/0000000419368956</rioxxterms:id>
</rioxxterms:contributor>
```
