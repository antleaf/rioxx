---
date: '2016-03-21T10:00:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:author
cardinality: One or more
requirement: Mandatory
metadata_profile: v1-5
---
The author of *the resource* may be a person, organisation or service, but is most commonly a person. This element **SHOULD** take an optional attribute called *id*, designed to hold an HTTP URI, if available, which uniquely identifies the author. Where there is more than one author, a separate rioxxterms:author element **MUST** be used for each.
As many authors may be entered as required. <del>If the author is a person and it is desired to record that person’s affiliation, the affiliation **SHOULD** be recorded as a rioxxterms:contributor element (see rioxxterms:contributor).</del> The ideal use of this element is to include both an HTTP URI in the *id* attribute, and a text string in the body of the element, thus:

    <rioxxterms:author id="identifier-for-this-author-entity">
        name-of-this-author-entity
    </rioxxterms:author>

Where the author is a person, the **RECOMMENDED** format is to add text in the form Last Name, First Name(s), and to include an ORCID ID, if known, in its HTTP URI form, e.g. 

    <rioxxterms:author id="http://orcid.org/0000-0002-1395-3092">
        Lawson, Gerald
    </rioxxterms:author>

Where the rioxxterms:author element appears multiple times for one record, it **CAN** be assumed that the order is significant, in that the first element describes the &#39;first named author&#39; of *the resource*. In order to make this more explicit, an extra attribute, *first-named-author*, **SHOULD** be used to indicate which of the rioxxterms:author elements describes the first named author of *the resource*, thus:

    <rioxxterms:author id="http://orcid.org/0000-0002-1395-3092" first-named-author="true">
        Lawson, Gerald
    </rioxxterms:author>
