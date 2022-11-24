---
date: '2022-06-21T14:26:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:author
cardinality: One or more
requirement: Mandatory
metadata_profile: v3-0-rc-2

---

The author of ***the resource*** may be a person, organisation or service, but is most commonly a person. This property **SHOULD** take an optional attribute called *uri*, which **MUST** contain a URI which uniquely identifies the author. Where there is more than one author, a separate *rioxxterms:author* property **MUST** be used for each. As many authors may be entered as required. 

<<<<<<< refs/remotes/antleaf/development
The ideal use of this property is to include both an HTTP(S) URI in the *uri* attribute and a text string in the body of the property, thus:
=======
The ideal use of this element is to include both an HTTP(S) URI in the *uri* attribute and a text string in the body of the element, thus:

> > > > > > > Refreshed changes: author, contributor, type

```xml
<rioxxterms:author uri="https-uri-for-this-author-entity">
    name-of-this-author-entity
</rioxxterms:author>
```

Where the author is a person, the **RECOMMENDED** format is to add text in the form Last Name, First Name(s), and to include a recognised persistent identifier scheme such as an [ORCID](https://orcid.org) ID, if known, in its HTTPS URI form, e.g. 

```xml
<rioxxterms:author uri="https://orcid.org/0000-0001-5305-9450">
    Riccardi, Annalisa
</rioxxterms:author>
```

Where the author is an organisation, the **RECOMMENDED** format is to add the official name of the organisation, and to include a recognised persistent identifier scheme in its HTTP(S) URI form. Such an identifier scheme might include [ISNI](https://isni.org), [Research Organization Registry](https://ror.org/), [Global Research Identifier Database](https://www.grid.ac/), [VIAF](http://viaf.org/) or [WikiData concept URI](https://www.wikidata.org/), e.g.

```xml
<rioxxterms:author uri="https://isni.org/isni/0000000419368139">
    University of Strathclyde
</rioxxterms:author>
```

Where the *rioxxterms:author* property appears multiple times for one record, it **CAN** be assumed that the order is significant, in that the first element describes the &#39;first named author&#39; of ***the resource***. In order to make this more explicit, an extra attribute, *first-named-author*, **SHOULD** be used to indicate which of the *rioxxterms:author* elements describes the first named author of ***the resource***, thus:

```xml
<rioxxterms:author uri="https://orcid.org/0000-0001-5305-9450" first-named-author="true">
    Riccardi, Annalisa
</rioxxterms:author>
```

Systems wishing to communicate the existece of multiple URIs for a single author **SHOULD** repeat `rioxxterms:author`. For example, a system wishing to expose both an ORCID and a VIAF entry in relation to a single author should represent the data as follows:

```xml
<rioxxterms:author uri="https://orcid.org/0000-0002-2362-4874">
    Uttamchandani, Deepak
</rioxxterms:author>
<rioxxterms:author uri="https://viaf.org/viaf/51771497">
    Uttamchandani, Deepak
</rioxxterms:author>
```
