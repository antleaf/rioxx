---
date: '2016-03-21T10:00:43+00:00'
draft: false
type: metadata_profile_property
title: free_to_read
cardinality: Zero or one
requirement: Optional
metadata_profile: v2-0-beta-1
---
This is defined in the [NISO Open Access Metadata and Indicators](http://www.niso.org/workrooms/oami/).

This element does not take a value - the semantics of *free_to_read* are conveyed by its presence or absence. This element may be modified by two optional attributes

* start_date
* end_date

Each of these attributes, if present, takes a date value which **MUST** be encoded using ISO 8601 (post&#8211;2004 versions) which follows the following format: YYYY-MM-DD.
Examples:

    <free_to_read start_date="2013-03-28" end_date="2014-04-30">
    <free_to_read start_date="2013-03-28">
    <free_to_read>

The absence of a *start_date* attribute implies that the meaning conveyed by the free_to_read element is current and immediate, unless an *end_date* attribute which is a date in the subjective past, is present in the element.

***Note that NISO have yet to specify a namespace for this element - RIOXX will adopt the NISO recommendation when it is made***
