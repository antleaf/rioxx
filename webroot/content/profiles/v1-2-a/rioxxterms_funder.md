---
date: '2016-03-21T10:00:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:funder
cardinality: One or more
requirement: Mandatory
metadata_profile: v1-2-a
---
The canonical name of the entity responsible for funding the resource being described by this RIOXX record **MUST** be recorded here as text. Where more than one funder exists, each **MUST** be entered as a separate instance of this field. A controlled list of funder names **SHOULD** be used. The list of funder names provided by the [FundRef](http://www.crossref.org/fundref/) service is **RECOMMENDED**

This element **SHOULD** take an optional attribute called *id*, designed to hold a machine-readable and unique identifier, if available, for the funder. Any ID entered here **MUST** be in a form which allows it to be parsed and recognised automatically. The FundRef ID (DOI) is **RECOMMENDED**. The ideal use of this element is to include both a machine-readable ID in the *id* attribute, and a text string in the body of the element, thus:

    <rioxxterms:funder id="http://dx.doi.org/10.13039/501100000690">
        Research Councils UK
    </rioxxterms:funder>
