---
date: '2022-03-31T10:00:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:project
cardinality: One or more
requirement: Optional
metadata_profile: v3-0-final
---
The purpose `rioxxterms:project` is to collect project ID(s), that relate to ***the resource***, together with any associated grant ID(s).

The element **MUST** contain one project ID, a globally unique identifier that identifies a project which is a direct outcome of the relevant grant ID.

The element accommodates the *grant_id* attribute. It is anticipated that this attribute will reflect the contents of `rioxxterms:grant` if used. 

## grant_id
A grant ID can take the form of an alphanumeric identifier provided by the funder in its original format or preferably an HTTP(S) URI, such as a grant identifier. In cases where ***the resource*** has been funded internally, an appropriate internal code might be used.

## Example

```xml
<rioxxterms:project
    grant="https://doi.org/10.35802/218671">
    https://all-suitable-project-idenitifier
</rioxxterms:project>
```

Where ***the resource*** is associated with more than one project ID, *rioxxterms:project* element **MUST** be added for each. This means that it is quite normal for a given *project_id* to appear in multiple instances of the `rioxxterms:project` element in a single RIOXX metadata record.
