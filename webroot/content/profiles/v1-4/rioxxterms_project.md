---
date: '2016-03-21T10:00:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:project
cardinality: One or more
requirement: Mandatory
metadata_profile: v1-4
---
This is designed to collect the project ID(s), issued by the funder(s), that relate to ***the resource***, together with the name and/or global identifier for the funder(s).

The element is an &#39;empty&#39; element, composed of three attributes, *project_id*, *funder_name* and *funder_id*. The *project_id* attribute, and one or both of *funder_name* and *funder_id* **MUST** be supplied.

## project_id

It is **REQUIRED** to use the alphanumeric identifier provided by the funder in its original format<del> e.g. ST/K001234/1</del>. In cases where ***the resource*** has been funded internally, an appropriate internal code might be used.

## funder_name
The canonical name of the entity responsible for funding ***the resource*** **SHOULD** be recorded here as text. A controlled list of funder names **MUST** be used for this. The list of funder names provided by the [FundRef](http://www.crossref.org/fundref/) service is **RECOMMENDED**

## funder_id
A globally unique identifier for the funder of ***the resource*** **SHOULD** be recorded here. Where possible, an HTTP URI **SHOULD** be used for this. It is **RECOMMENDED** that a DOI (in its HTTP URI form) made available by the [FundRef](http://www.crossref.org/fundref/) service is used for this.

## Example

    <rioxxterms:project
        project_id="ST/K001234/1"
        funder_name="Research Councils UK"
        funder_id="http://dx.doi.org/10.13039/501100000690"
    />

This element may be included multiple times in one record, so where ***the resource*** has been funded by more than one funder, a separate *rioxxterms:project* element **MUST** be added for each. Similarly, where several project IDs have been attached to ***the resource***, a separate *rioxxterms:project* element **MUST** be added for each.

This means that it is quite normal for a given *funder_name*, *funder_id* or *project_id* to appear in multiple instances of the *rioxxterms:project* element in a single RIOXX metadata record.
