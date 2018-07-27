---
date: '2016-03-21T10:00:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:contributor
cardinality: Zero or more
requirement: Optional
metadata_profile: v1-1
---
This field is designed to describe an entity – for example the name of a person, organisation or service – responsible for making contributions to the content of the resource. As many rioxxterms:contributor elements may be entered as required. If the contributor is a person and it is desired to record that person's affiliation, the affiliation **MUST** be recorded as a separate rioxxterms:contributor element. This element **SHOULD** take an optional attribute called *id*, designed to hold a machine-readable and unique identifier, if available, for the contributor. Any ID entered here **MUST** be in a form which allows it to be parsed and recognised automatically. The ideal use of this element is to include both a machine-readable ID in the *id* attribute, and a text string in the body of the element, thus:

    <rioxxterms:contributor id="identifier-for-this-contributor-entity">
        name-of-this-contributor-entity
    </rioxxterms:contributor>

Where the contributor is a person, the **RECOMMENDED** format is to add text in the form Last Name, First Name(s), and to include an ORCID ID, if known, in its HTTP URI form, e.g.

    <rioxxterms:contributor id="http://orcid.org/0000-0002-1395-3092">
        Lawson, Gerald
    </rioxxterms:contributor>
