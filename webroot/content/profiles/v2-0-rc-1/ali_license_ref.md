---
date: '2016-03-21T10:00:43+00:00'
draft: false
type: metadata_profile_property
title: ali:license_ref
cardinality: One or more
requirement: Mandatory
metadata_profile: v2-0-rc-1
---
This is defined in the [NISO Open Access Metadata and Indicators](http://www.niso.org/workrooms/oami/). This element **MUST** take an HTTP URI for its value. This HTTP URI **MUST** point to a resource which expresses the license terms specifying how ***the resource*** may be used.

This element **MUST** include the attribute:

* start_date

This attribute takes a date value which **MUST** be encoded using ISO 8601 (post&#8211;2004 versions) which follows the following format: YYYY-MM-DD.

This atribute is used to indicate the date upon which this license takes effect. Multiple *ali:license_ref* elements may be included. Where several such elements are included, the one with the *start_date* attribute indicating the most recent date takes precedence.

Example:
    
    <ali:license_ref start_date="2015-02-17">http://creativecommons.org/licenses/by/3.0/deed.en_US</ali:license_ref>


This approach allows the expression of &#39;embargoes&#39;, where a particular license takes effect at a date in the subjective future.

***Note that NISO have yet to specify a namespace for this element - RIOXX will adopt the NISO recommendation when it is made***
