---
date: '2016-03-21T10:00:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:version-of-record
cardinality: Zero or one
requirement: Recommended
metadata_profile: v1-3
---
This field MUST contain a globally unique and persistent identifier for the published version of the resource being described. The identifier SHOULD be an HTTP URI that can be de-referenced (and is, thus, actionable). If a DOI has been issued by the publisher then this *MUST* be used. Such a DOI **MUST** be represented in its HTTP form, for example:

    <rioxxterms:version-of-record>
        http://dx.doi.org/10.1006/jmbi.1995.0238
    </rioxxterms:version-of-record>
