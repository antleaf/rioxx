---
date: '2016-03-21T10:00:43+00:00'
draft: false
type: metadata_profile_property
title: license_ref
cardinality: One or one
requirement: Mandatory
metadata_profile: v1-2-a
---
This is defined in the [NISO Open Access Metadata and Indicators](http://www.niso.org/workrooms/oami/). This element **MUST** take an HTTP URI for its value. This HTTP URI **MUST** point to a resource which expresses the license terms specifying how the resource being described in the RIOXX record may be used.

This element **MAY** include an optional attribute:

* start_date

This attribute, if present, takes a date value which **MUST** be encoded using ISO 8601 (post&#8211;2004 versions) which follows the following format: YYYY-MM-DD.

This atribute is used to indicate the date upon which this license takes effect. Multiple <license_ref> elements may be included. Where several such elements are included, the one with the start_date attribute indicating the most recent date takes precendence.
A <license_ref> element with a start_date element takes precedence over a <license_ref> element without a start_date.

A single RIOXX record **MUST NOT** have more than one <license_ref> element without a start_date

Examples:

    <license_ref>http://www.samplejournal.org/license_v1.html</license_ref>
    
    <license_ref start_date="2015-02-17">http://creativecommons.org/licenses/by/3.0/deed.en_US</license_ref>


This approach allows the expression of 'embargoes', where a particular license takes effect at a future date.
