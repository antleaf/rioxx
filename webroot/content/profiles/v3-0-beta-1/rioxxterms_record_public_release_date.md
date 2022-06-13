---
date: '2020-10-08T10:00:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:record_public_release_date
cardinality: Zero or one
requirement: Optional
metadata_profile: v3-0-draft
---
This element takes the date upon which *metadata* about ***the resource*** being described was first made publicly visible. Element content **MUST** be encoded according to the [W3CDTF](https://www.w3.org/TR/NOTE-datetime) (a profile of [ISO 8601](https://www.iso.org/standard/40874.html)) which typically follows the following format: YYYY-MM-DD.

Examples:
```xml
<rioxxterms:record_public_release_date>
    2020-10-02
</rioxxterms:record_public_release_date>
```

or

```xml
<rioxxterms:record_public_release_date>
    2020-09-29T19:20+01:00
</rioxxterms:record_public_release_date>
```


It is anticipated that in many circumstances `rioxxterms:record_public_release_date` will be captured and exposed in repository metadata prior to availability of related resources such as the "full text" for a publication; for example as the result of a delay in depositing the full text, or where it is under temporary embargo or temporary dark archiving. 

