---
date: '2022-11-03T11:00:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:project
cardinality: Zero or more
requirement: Optional
metadata_profile: v3-0-draft-2
---
The purpose of `rioxxterms:project` is to collect project ID(s), that relate to *the resource*.

When present, the `rioxxterms:project` property **MUST** contain one project ID, a globally unique persistent identifier that identifies a project. Examples might include:

* a local identifier rendered as a URI
* a [RAiD handle](https://www.raid.org.au). 

## Example

```xml
<rioxxterms:project>
    https://handle.net/10378.1/1590366
</rioxxterms:project>
```

Where *the resource* is associated with more than one project ID, a `rioxxterms:project` property can be added for each. This means that it is permissible for multiple instances of the `rioxxterms:project` property to appear in a single Rioxx metadata record.


