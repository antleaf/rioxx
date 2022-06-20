---
date: '2016-03-21T10:00:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:version_of_record
cardinality: Zero or one
requirement: Recommended
metadata_profile: v2-0-beta-1
---
This field **MUST** contain an HTTP URI which is a persistent identifier for the published version of ***the resource***. If a DOI has been issued by the publisher then this *MUST* be used. Such a DOI **MUST** be represented in its HTTP form, for example:

    <rioxxterms:version_of_record>
        http://dx.doi.org/10.1006/jmbi.1995.0238
    </rioxxterms:version_of_record>
