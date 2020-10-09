---
date: '2016-03-21T10:00:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:publication_date
cardinality: Zero or one
requirement: Optional
metadata_profile: v2-0-final
---
This element takes the publication date of ***the resource*** in the form in which it would be cited. This element is not used in a RIOXX context but allows for a RIOXX record to become a reasonable bibliographic record for ***the resource***. This is a free-text field.

Examples:

    <rioxxterms:publication_date>
        2011-02-23
    </rioxxterms:publication_date>
    
    <rioxxterms:publication_date>
        Spring, 2010
    </rioxxterms:publication_date>


As RIOXX is primarily concerned with such issues as compliance with funders' mandates and licensing of open access publications, the critical dates for the assertion of compliance are those held in the *start_date* attributes of the *ali:license_ref* elements.
