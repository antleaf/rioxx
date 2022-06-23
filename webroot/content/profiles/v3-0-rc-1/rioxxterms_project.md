---
date: '2022-06-13T11:00:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:project
cardinality: One or more
requirement: Optional
metadata_profile: v3-0-rc-1
---
The purpose of `rioxxterms:project` is to collect project ID(s), that relate to ***the resource***.

The `rioxxterms:project` property **MUST** contain one project ID, a globally unique persistent identifier that identifies a project, such as a local identifier rendered as a persistent identifier or a [RAiD handle](https://www.raid.org.au). 

## Example

```xml
<rioxxterms:project>
    https://handle.net/10378.1/1590366
</rioxxterms:project>
```

Where ***the resource*** is associated with more than one project ID, a *rioxxterms:project* property **MUST** be added for each. This means that it is permissible for multiple instances of the `rioxxterms:project` property to appear in a single Rioxx metadata record.


