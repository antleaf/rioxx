---
date: '2016-03-21T10:00:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:contributor
cardinality: Zero or more
requirement: Optional
metadata_profile: v2-0-final_basic
---
This field is designed to describe an entity – for example the name of a person, organisation or service – responsible for making contributions to the content of ***the resource***. As many rioxxterms:contributor elements may be entered as required. This element **SHOULD** take an optional attribute called *id*, which **MUST** contain an HTTP URI which uniquely identifies the contributor. The ideal use of this element is to include both an HTTP URI in the *id* attribute, and a text string in the body of the element, thus:

    <rioxxterms:contributor id="http-uri-for-this-contributor-entity">
        name-of-this-contributor-entity
    </rioxxterms:contributor>

Where the contributor is a person, the **RECOMMENDED** format is to add text in the form Last Name, First Name(s), and to include an [ORCID](http://orcid.org) ID, if known, in its HTTP URI form, e.g.

    <rioxxterms:contributor id="http://orcid.org/0000-0002-1395-3092">
        Lawson, Gerald
    </rioxxterms:contributor>

Where the contributor is an organisation, the **RECOMMENDED** format is to add the official name of the organisation, and to include an [ISNI](http://isni.org) ID, if known, in its HTTP URI form, e.g.

    <rioxxterms:contributor id="http://isni.org/isni/0000000419367988">
        University of Edinburgh
    </rioxxterms:contributor>
