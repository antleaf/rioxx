---
date: '2022-06-17T15:00:43+00:00'
draft: false
type: metadata_profile_property
title: ali:license_ref
cardinality: One or more
requirement: Mandatory
metadata_profile: v3-0-rc-1
---
This is defined in the [NISO Open Access Metadata and Indicators](https://www.niso.org/workrooms/ali/). This property **MUST** take an HTTP(S) URI for its value. This URI **MUST** point to a resource which expresses the license terms specifying how ***the resource*** may be used.

property content **MUST** be encoded according to the [W3CDTF](https://www.w3.org/TR/NOTE-datetime) (a profile of [ISO 8601](https://www.iso.org/standard/40874.html)) which typically follows the following format: YYYY-MM-DD.

This property **MUST** include the attribute:

* start_date

This attribute indicates the date upon which this license takes effect. Multiple *ali:license_ref* properties may be included. Where several such properties are included, the one with the *start_date* attribute indicating the most recent date takes precedence.

Example:

```xml
<ali:license_ref start_date="2020-11-17">
    https://creativecommons.org/licenses/by/4.0
</ali:license_ref>
```

This approach allows the expression of &#39;embargoes&#39;, where a particular license takes effect at a date in the subjective future.

In the absence of any other license, the copyright holder reserves all rights automatically. As a convenience, Rioxx provides two URLs which may be used to explicitly convey this state:

* [https://www.rioxx.net/licenses/all-rights-reserved](/licenses/all-rights-reserved)
* [https://www.rioxx.net/licenses/under-embargo-all-rights-reserved](/licenses/under-embargo-all-rights-reserved)
