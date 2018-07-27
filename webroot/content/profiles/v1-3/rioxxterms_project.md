---
date: '2016-03-21T10:00:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:project
cardinality: One or more
requirement: Mandatory
metadata_profile: v1-3
---
This is designed to collect the project IDs issued by funders that relate to the current resource, together with the name and/or global identifier for the funder.

The element is an 'empty' element, composed of three attributes, *project_id*, *funder_name* and *funder_id*. The *project_id* attribute, and one or both of *funder_name* and *funder_id* **MUST** be supplied.

### project_id

It is **REQUIRED** to use the alphanumeric identifier provided by the funder in its original format e.g. ST/K001234/1. Sometimes publications have more than one project ID associated with them; these **MUST** be recorded using separate instances of rioxxterms:project. In cases where projects have been funded internally, use whichever internal code is appropriate.

### funder_name
The canonical name of the entity responsible for funding the resource being described by this RIOXX record **SHOULD** be recorded here as text. A controlled list of funder names **SHOULD** be used for this. The list of funder names provided by the [FundRef](http://www.crossref.org/fundref/) service is **RECOMMENDED**

### funder_id
A globally unique identifier for the entity responsible for funding the resource being described by this RIOXX record **SHOULD** be recorded here. Where possible, an HTTP URI **SHOULD** be used for this. It is **RECOMMENDED** that the DOI (in its HTTP URI form) made available by the [FundRef](http://www.crossref.org/fundref/) service is used for this.

## Example

    <rioxxterms:project
        project_id="ST/K001234/1"
        funder_name="Research Councils UK"
        funder_id="http://dx.doi.org/10.13039/501100000690"
    />

This element may be included multiple times in one record, so where a resource has been funded by more than one funder, a separate *rioxxterms:project* element **MUST** be added for each. Similarly, where several project IDs have been attached to the resource, a separate *rioxxterms:project* element **MUST** be added for each.
