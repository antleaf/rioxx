---
categories: []
date: 2015-10-29T07:19:39Z
description: ""
draft: false
tags: []
title: RCUK RIOXX Application Profile Version 0.8
topics: []
aliases:
  - "/v0-8/"
status: obsolete
layout: single_special_case
---

<table border="1" cellspacing="0" cellpadding="0">
<tbody>
<tr>
<th valign="top"><b>Element</b></td>
<th valign="top"><b>Inclusion</b></td>
<th valign="top"><b>Description</b></td>
<th valign="top"><b>Roadmap</b></td>
<td>
&nbsp;
</td>
</tr>
<tr>
<td class="nowrap">dc:title</td>
<td class="nowrap">Mandatory</td>
<td>
This refers to the resource’s title and any sub-titles. Title should be entered using free text. Title is the form of words by which a resource will be formally known and should be represented using the original spelling and wording. The recommended format for expressing subtitles is <em>Title:Subtitle</em>
</td>
<td>
&nbsp;
</td>
</tr>
<tr>
<td class="nowrap">dc:creator</td>
<td class="nowrap">Mandatory</td>
<td>
The creator of a resource may be a person, organisation or service. Where there is more than one creator, use a separate dc:creator element for each one. Enter as many creators as required.

If the creator is a person and it is desired to record that person's affiliation, the affiliation should be recorded as a dc:contributor element (see below).

Where the creator is a person, the recommended format is either to add text in the form <em>Last Name, First Name(s), </em> or to add a unique identifier from a recognised system such as <a href="http://about.orcid.org">ORCID</a>. ORCID IDs should be entered in their HTTP URI form, e.g. http://orcid.org/0000-0003-1541-5631
</td>
<td>
&nbsp;
</td>
</tr>
<tr>
<td class="nowrap">dc:identifier</td>
<td class="nowrap">Mandatory</td>
<td>
A globally unique identifier for the resource. The use of an HTTP URI that can be de-referenced (and is, thus, actionable) is recommended. A commonly-used example is a publisher’s DOI, in it's HTTP form - e.g. http://dx.doi.org/10.1006/jmbi.1995.0238

It is strongly recommended that this identifier should point to the actual resource being described by a RIOXX record (typically a PDF file), rather than to an intermediary resource such as a repository web page.
</td>
<td>
We anticipate future work to support repositories in making this identifier point reliably to the resource being described, rather than to, for example, an intermediate web page.
</td>
</tr>
<tr>
<td class="nowrap">dc:source</td>
<td class="nowrap">Mandatory</td>
<td>
The source label describes a resource from which the current resource is derived (in whole or in part).  It is recommended that the source is referenced using a unique identifier from a recognised system e.g. the unique 8-digit International Standard Serial Numbers (ISSN) assigned to print and electronic periodicals.
</td>
<td>
&nbsp;
</td>
</tr>
<tr>
<td class="nowrap">dc:language</td>
<td class="nowrap">Mandatory</td>
<td>
This refers to the primary language in which the content of the resource is presented. The element can be repeated if the resource contains multiple languages. A coded value or text string may be used. It is, however, recommended that the values used for this element conform to <a href="http://en.wikipedia.org/wiki/ISO_639-3">ISO 639-3</a>. This offers two and three letter tags e.g. “en” or “eng” for English and “en-GB” for English used in the UK.
</td>
<td>
&nbsp;
</td>
</tr>
<tr>
<td class="nowrap">rioxxterms:projectid</td>
<td class="nowrap">Mandatory</td>
<td>
This is an addition to Dublin Core’s fifteen generic elements and is designed to collect the grant numbers issued by funders to Principal Investigators that relate to the current resource. It is mandatory to use the alphanumeric identifier provided by the funder in its original format e.g. ST/K001234/1 (denoting an STFC award). Sometimes publications have more than one funder associated with them; these should be recorded using separate iterations of rioxxterms.projectid. In cases where projects have been funded internally, use whichever internal code is appropriate.
</td>
<td>
&nbsp;
</td>
</tr>
<tr>
<td class="nowrap">rioxxterms:funder</td>
<td class="nowrap">Mandatory</td>
<td>
This is an addition to Dublin Core’s fifteen generic elements and is designed to collect the funder’s name. It is recommended that you use free text to record the funder’s name in its preferred format (normally that indicated in the grant award notice).
</td>
<td>
Work is under way to facilitate access to an international directory of funder names. When this becomes available it will be mandatory to use the unique funder identity number described in the directory.
</td>
</tr>
<tr>
<td class="nowrap">dcterms:issued</td>
<td class="nowrap">Mandatory</td>
<td>
The publication date of the resource. It is recommended that date is encoded using ISO 8601 (post-2004 versions) which follows the following format: YYYY-MM-DD.  Year (YYYY) or year and month (YYYY-MM) may be used if the full date is not known.
</td>
<td>
&nbsp;
</td>
</tr>
<tr>
<td class="nowrap">dc:format</td>
<td class="nowrap">Recommended</td>
<td>
This refers to the form of the resource, physical or digital and can refer to the media-type or dimensions of the resource. It is recommended that the IANA registered list of Internet Media Types (MIME types) be used. If more than one category is needed to describe a single resource, use separate iterations of the dc:format element.
</td>
<td>
&nbsp;
</td>
</tr>
<tr>
<td class="nowrap">dc:publisher</td>
<td class="nowrap">Recommended</td>
<td>
A free text string giving the name of the entity responsible for making the version of record of a resource available. This could be a person, organisation or service.
</td>
<td>
&nbsp;
</td>
</tr>
<tr>
<td class="nowrap">dc:description</td>
<td class="nowrap">Recommended</td>
<td>
This field may be indexed and its contents presented to people conducting searches. The goal is to describe the content of the resource using free text. It is recommended that an English language abstract be used where available. HTML or other markup tags should not be included in this field.
</td>
<td>
&nbsp;
</td>
</tr>
<tr>
<td class="nowrap">dc:subject</td>
<td class="nowrap">Recommended</td>
<td>
Normally keywords, phrases or classification codes are used to describe the topic of the resource. If using free text, avoid using general keywords. The recommendation is to use a formal classification scheme or controlled vocabulary e.g Library of Congress Classification Numbers or Medical Subject Headings (MeSH). When including terms from multiple vocabularies, use separate element iterations. If multiple vocabulary terms or keywords are used, either separate terms with semi-colons or use separate iterations of the Subject element.
</td>
<td>
&nbsp;
</td>
</tr>
<tr>
<td class="nowrap">dc:coverage</td>
<td class="nowrap">Optional</td>
<td>
This refers to the scope or extent of the content of the resource. It may include jurisdictional, temporal or spatial information. It is recommended that, where possible, a recognised globally unique identifier is used, such as the Thesaurus of Geographic Names, but free text may be used. For example, the place of publication may be recorded.
</td>
<td>
&nbsp;
</td>
</tr>
<tr>
<td class="nowrap">dc:rights</td>
<td class="nowrap">Optional</td>
<td>
At present there is no agreed vocabulary that describes intellectual property or other property rights with respect to open access full text resources. This field is commonly ignored at present.
</td>
<td>
Work is under way to develop consensus on a controlled vocabulary that describes rights to open access items as well as the associated issues of Creative Commons licenses and embargo periods.  Once this work concludes the appropriate use of this element is expected to become mandatory.
</td>
</tr>
<tr>
<td class="nowrap">dc:audience</td>
<td class="nowrap">Optional</td>
<td>
This field is designed to contain information about the group for which the resource is intended or useful. There are no established vocabularies but sometimes creators or publishers indicate the intended audience. Note that the Research Outcomes System (ROS) used by most of the UK’s Research Councils track whether a resource is for a “non-academic audience” (with a drop-down list of possible selections) and whether a resource is for an “international audience”. In the absence of alternative formal vocabularies, following the ROS lead is a reasonable course of action.
</td>
<td>
The development of a controlled vocabulary for audience is likely to be recommended for Phase 2 of the RIOXX project.
</td>
</tr>
<tr>
<td class="nowrap">dc:type</td>
<td class="nowrap">Optional</td>
<td>
Type refers to the nature or genre of the content of the resource and can be entered as free text. Take care not to confuse this with dc:format.
</td>
<td>
The development of a controlled vocabulary is likely to be recommended for Phase 2 of the RIOXX project.
</td>
</tr>
<tr>
<td class="nowrap">dc:contributor</td>
<td class="nowrap">Optional</td>
<td>
This element is designed to describe the entity – for example the name of a person, organisation or service – responsible for making contributions to the content of the resource. Enter as many dc:contributor elements as required.

If the contributor is a person and it is desired to record that person's affiliation, the affiliation should be recorded as a separate dc:contributor element.

Where the contributor is a person, the recommended format is either to add text in the form <em>Last Name, First Name(s), </em> or to add a unique identifier from a recognised system such as <a href="http://about.orcid.org">ORCID</a>. ORCID IDs should be entered in their HTTP URI form, e.g. http://orcid.org/0000-0003-1541-5631
</td>
<td>
&nbsp;
</td>
</tr>
</tbody>
</table>
