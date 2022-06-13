---
date: '2016-03-21T10:00:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:project
cardinality: One or more
requirement: Mandatory
metadata_profile: v2-0-final
---
This is designed to collect the project ID(s), issued by the funder(s), that relate to ***the resource***, together with the name and/or global identifier for the funder(s).

The element **MUST** contain one project ID, an alphanumeric identifier provided by the funder in its original format. In cases where ***the resource*** has been funded internally, an appropriate internal code might be used.

The element takes two attributes, *funder_name* and *funder_id*. One or both of *funder_name* and *funder_id* **MUST** be supplied.

## funder_name
The canonical name of the entity responsible for funding ***the resource*** **SHOULD** be recorded here as text.

## funder_id
A globally unique identifier for the funder of ***the resource*** **SHOULD** be recorded here. An HTTP URI **MUST** be used for this. It is **RECOMMENDED** that one of the following identifier schemes is used:

* an [ISNI](http://isni.org) ID
* a DOI (in its HTTP URI form) made available by [FundRef](http://www.crossref.org/fundref/)

## Example

    <rioxxterms:project
        funder_name="Engineering and Physical Sciences Research Council"
        funder_id="http://isni.org/isni/0000000403948681"
    >
        EP/K023195/1
    </rioxxterms:project>

or

    <rioxxterms:project
        funder_name="Engineering and Physical Sciences Research Council"
        funder_id="http://dx.doi.org/10.13039/501100000266"
    >
        EP/K023195/1
    </rioxxterms:project>

Where ***the resource*** has been funded by more than one funder a separate *rioxxterms:project* element **MUST** be added for each. Similarly, where several project IDs provided by the same funder have been attached to ***the resource***, a separate *rioxxterms:project* element **MUST** be added for each.

This means that it is quite normal for a given *funder_name*, *funder_id* or *project_id* to appear in multiple instances of the *rioxxterms:project* element in a single RIOXX metadata record.
