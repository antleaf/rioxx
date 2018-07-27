---
date: '2016-03-21T10:00:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:contributor
cardinality: Zero or more
requirement: Optional
metadata_profile: v1-5
---
This field is designed to describe an entity – for example the name of a person, organisation or service – responsible for making contributions to the content of ***the resource***. As many rioxxterms:contributor elements may be entered as required. <del>If the contributor is a person and it is desired to record that person&#39;s affiliation, the affiliation **MUST** be recorded as a separate rioxxterms:contributor element.</del> This element **SHOULD** take an optional attribute called *id*, designed to hold an HTTP URI, if available, which uniquely identifies the contributor. The ideal use of this element is to include both an HTTP URI in the *id* attribute, and a text string in the body of the element, thus:

    <rioxxterms:contributor id="identifier-for-this-contributor-entity">
        name-of-this-contributor-entity
    </rioxxterms:contributor>

Where the contributor is a person, the **RECOMMENDED** format is to add text in the form Last Name, First Name(s), and to include an ORCID ID, if known, in its HTTP URI form, e.g.

    <rioxxterms:contributor id="http://orcid.org/0000-0002-1395-3092">
        Lawson, Gerald
    </rioxxterms:contributor>
