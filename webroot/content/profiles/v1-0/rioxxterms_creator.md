---
date: '2016-03-21T10:00:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:creator
cardinality: One or more
requirement: Mandatory
metadata_profile: v1-0
---
The creator of a resource may be a person, organisation or service. Where there is more than one creator, a separate rioxxterms:creator element **MUST** be used for each one.
As many creators may be entered as required. If the creator is a person and it is desired to record that person’s affiliation, the affiliation **SHOULD** be recorded as a rioxxterms:creator element (see rioxxterms:creator).
This element **SHOULD** take an optional attribute called *id*, designed to hold a machine-readable and unique identifier, if available, for the creator. Any ID entered here **MUST** be in a form which allows it to be parsed and recognised automatically. The ideal use of this element is to include both a machine-readable ID in the *id* attribute, and a text string in the body of the element, thus:

    <rioxxterms:creator id="identifier-for-this-creator-entity">
        name-of-this-creator-entity
    </rioxxterms:creator>

Where the creator is a person, the **RECOMMENDED** format is to add text in the form Last Name, First Name(s), and to include an ORCID ID, if known, in its HTTP URI form, e.g. 

    <rioxxterms:creator id="http://orcid.org/0000-0002-1395-3092">
        Lawson, Gerald
    </rioxxterms:creator>
