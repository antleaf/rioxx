---
date: '2022-03-25T15:38:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:grant
cardinality: One or more
requirement: Optional
metadata_profile: v3-0-final
---
The purpose of `rioxxterms:grant` is to collect grant ID(s), issued by the relevant funder(s), that relate to ***the resource*** being described, together with the name and/or global identifier for the funder(s) and (where available) directly funded projects.

The element **MUST** contain one grant ID. A grant ID can take the form of an alphanumeric identifier provided by the funder in its original format or preferably an HTTP(S) URI. In cases where ***the resource*** has been funded internally, an appropriate internal code might be used.

The element takes three attributes, *funder_name*, *funder_id* and *project_id*. One or both of *funder_name* and *funder_id* **MUST** be supplied. *project_id* is **OPTIONAL**.

## funder_name
The canonical name of the entity responsible for funding ***the resource*** **SHOULD** be recorded here as text.

## funder_id
A globally unique identifier for the funder of ***the resource*** **SHOULD** be recorded here. An HTTP(S) URI **MUST** be used for this. It is **RECOMMENDED** that one of the following identifier schemes is used:

* an [ISNI](https://isni.org) identifier
* a DOI (in its HTTPS URI form) made available by [FundRef](https://www.crossref.org/fundref/)
* a ROR identifier (in its HTTPS URI form) made available by the [Research Organization Registry](https://ror.org/)
* a GRID idenitifier (in its HTTPS URI form) made available by the [Global Research Identifier Database](https://www.grid.ac/) 

## project_id
A globally unique identifier that identifies a project which is a direct outcome of the relevant grant ID. This attribute is **OPTIONAL** but **MUST** use an HTTP(S) URI if included, such as a local identifier rendered as a persistent identifier or a [RAiD handle](https://www.raid.org.au). It is anticipated that this attribute will reflect the contents of `rioxxterms:project` if used. 

## Examples

```xml
<rioxxterms:grant
    funder_name="Wellcome Trust"
    funder_id="https://isni.org/isni/0000000404277672">
    https://doi.org/10.35802/218671
</rioxxterms:project>
```
or

```xml
<rioxxterms:grant
    funder_name="Arts and Humanities Research Council"
    funder_id="https://ror.org/0505m1554"
    project_id="https://handle.net/10378.1/1590366">
    AH/W007622/1
</rioxxterms:project>
```

Where ***the resource*** has been funded by more than one funder a separate *rioxxterms:grant* element **MUST** be added for each. Similarly, where several grant IDs provided by the same funder have been attached to ***the resource***, a separate *rioxxterms:grant* element **MUST** be added for each.

This means that it is quite normal for a given *funder_name*, *funder_id* or *project_id* to appear in multiple instances of the *rioxxterms:grant* element in a single RIOXX metadata record.
