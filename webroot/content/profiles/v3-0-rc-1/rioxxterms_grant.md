---
date: '2022-06-13T11:38:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:grant
cardinality: One or more
requirement: Optional
metadata_profile: v3-0-rc-1
---
The purpose of `rioxxterms:grant` is to collect grant ID(s), issued by the relevant funder(s), that relate to ***the resource*** being described, together with the name and/or global identifier for the funder(s).

The property **MUST** contain one grant ID. A grant ID can take the form of any identifier provided by the funder, preferably represented as an HTTP(S) URI. In cases where ***the resource*** has been funded internally, an appropriate internal code might be used.

The property takes two attributes: *funder_name* and *funder_id*. One or both of *funder_name* and *funder_id* **MUST** be supplied.

## funder_name
The canonical name of the entity responsible for funding ***the resource*** **SHOULD** be recorded here as text.

## funder_id
A globally unique identifier for the funder of ***the resource*** **SHOULD** be recorded here. An HTTP(S) URI **MUST** be used for this. It is **RECOMMENDED** that one of the following identifier schemes is used:

* an [ISNI](https://isni.org) identifier
* a DOI (in its HTTPS URI form) made available by [FundRef](https://www.crossref.org/fundref/)
* a ROR identifier (in its HTTPS URI form) made available by the [Research Organization Registry](https://ror.org/)
* a GRID identifier (in its HTTPS URI form) made available by the [Global Research Identifier Database](https://www.grid.ac/) 

## Examples

```xml
<rioxxterms:grant
    funder_name="Wellcome Trust"
    funder_id="https://isni.org/isni/0000000404277672">
    https://doi.org/10.35802/218671
</rioxxterms:grant>
```
or

```xml
<rioxxterms:grant
    funder_name="Arts and Humanities Research Council"
    funder_id="https://ror.org/0505m1554">
    AH/W007622/1
</rioxxterms:grant>
```

Where ***the resource*** has been funded by more than one funder a separate *rioxxterms:grant* property **MUST** be added for each. Similarly, where several grant IDs provided by the same funder have been attached to ***the resource***, a separate *rioxxterms:grant* property **MUST** be added for each.

This means that it is permissible for a given *funder_name* or *funder_id* to appear in multiple instances of the *rioxxterms:grant* property in a single Rioxx metadata record.
