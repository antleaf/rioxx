---
date: '2021-01-15T14:00:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:publication_date
cardinality: Zero or one
requirement: Optional
metadata_profile: v3-0-draft
---
This element takes the publication date of ***the resource*** in the form in which it would be cited. This allows for a RIOXX record to become a reasonable bibliographic record for ***the resource***. 

Where possible the element content **SHOULD** be encoded according to the [W3CDTF](https://www.w3.org/TR/NOTE-datetime) (a profile of [ISO 8601](https://www.iso.org/standard/40874.html)) which typically follows the following format: YYYY-MM-DD. 

Example:
```xml
<rioxxterms:publication_date>
    2011-02-23
</rioxxterms:publication_date>
```

As RIOXX can form a mechanism for establishing compliance with funders' mandates and licensing of open access publications, the critical dates for the assertion of compliance are those held in the *start_date* attributes of the *ali:license_ref* elements.

It is acknowledged that the publication date conventions of certain publishers vary, making the identification of precise publication dates problematic, especially in instances where a publisher assigns a resource to a seasonal issue date, e.g. Spring 2020, Winter 2019, etc. To maintain adherence to the above noted encoding conventions, resources with publication dates assigned to seasonal issues should be expressed according to the following convention, with months expressed as per:

- 01 = winter (beginning of year)
- 04 = spring
- 07 = summer
- 10 = autumn
- 12 = winter (end of year)

Examples:

*Spring 2020*

```xml
<rioxxterms:publication_date>
    2020-04
</rioxxterms:publication_date>
```

*Winter 2019 (end of year)*
```xml
<rioxxterms:publication_date>
    2019-12
</rioxxterms:publication_date>
```


