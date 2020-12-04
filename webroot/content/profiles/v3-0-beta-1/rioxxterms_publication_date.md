---
date: '2020-12-04T10:00:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:publication_date
cardinality: Zero or one
requirement: Optional
metadata_profile: v3-0-draft
---
This element takes the publication date of ***the resource*** in the form in which it would be cited. This allows for a RIOXX record to become a reasonable bibliographic record for ***the resource***. 

Where possible the element content **SHOULD** be encoded according to the [W3CDTF](https://www.w3.org/TR/NOTE-datetime) (a profile of [ISO 8601](https://www.iso.org/standard/40874.html)) which typically follows the following format: YYYY-MM-DD. 

Example:

    <rioxxterms:publication_date>
        2011-02-23
    </rioxxterms:publication_date>

As RIOXX can form a mechanism for establishing compliance with funders' mandates and licensing of open access publications, the critical dates for the assertion of compliance are those held in the *start_date* attributes of the *ali:license_ref* elements.

It is acknowledged that the publication date conventions of certain publishers vary, making the identification of a precise publication date difficult. 

Examples:

    <rioxxterms:publication_date>
        @@@@@@@@@@@
    </rioxxterms:publication_date>
    
    <rioxxterms:publication_date>
        Spring, 2010
    </rioxxterms:publication_date>

@@@Based on REF guidance, ISO8601 could be followed, obviating the need for this to be a free-text field.

