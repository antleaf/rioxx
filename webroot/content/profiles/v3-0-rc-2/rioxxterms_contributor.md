---
date: '2022-11-21T14:58:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:contributor
cardinality: Zero or more
requirement: Optional
metadata_profile: v3-0-rc-2

---

This field is designed to describe an entity – for example the name of a person, organisation or service – responsible for making contributions to the content of ***the resource***. As many rioxxterms:contributor properties may be entered as required. This property **SHOULD** take an optional attribute called *uri*, which **MUST** contain a URI which uniquely identifies the contributor. The ideal use of this property is to include both an HTTP(S) URI in the *uri* attribute, and a text string in the body of the property, thus:

```xml
<rioxxterms:contributor uri="https-uri-for-this-contributor-entity">
    name-of-this-contributor-entity
</rioxxterms:contributor>
```

Where the contributor is a person, the **RECOMMENDED** format is to add text in the form Last Name, First Name(s), and to include a recognised persistent identifier scheme, such as an [ORCID](http://orcid.org) ID, if known, in its HTTPS URI form, e.g.

```xml
<rioxxterms:contributor uri="https://orcid.org/0000-0002-1919-4138">
    Milgrom, Paul
</rioxxterms:contributor>
```

Where the contributor is an organisation, the **RECOMMENDED** format is to add the official name of the organisation, and to include a recognised persistent identifier scheme in its HTTP(S) URI form. Such an identifier scheme might include [ISNI](https://isni.org), [Research Organization Registry](https://ror.org/), [Global Research Identifier Database](https://www.grid.ac/), [VIAF](http://viaf.org/) or [WikiData concept URI](https://www.wikidata.org/), e.g.

```xml
<rioxxterms:contributor uri="https://isni.org/isni/0000000419368956">
    Stanford University
</rioxxterms:contributor>
```

Systems wishing to communicate the existece of multiple URIs for a single contributor **SHOULD** repeat `rioxxterms:contributor`. For example, a system wishing to expose both an ISNI and a VIAF entry in relation to a single contributor should represent the data as follows:

```xml
<rioxxterms:contributor uri="https://isni.org/isni/0000000056397298">
    Cox, Brian
</rioxxterms:contributor>
<rioxxterms:contributor uri="https://viaf.org/viaf/83469771">
    Cox, Brian
</rioxxterms:contributor>
```
