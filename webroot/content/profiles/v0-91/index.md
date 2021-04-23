---
categories: []
date: 2015-10-29T07:19:39Z
description: ""
draft: false
tags: []
title: RCUK RIOXX Application Profile Version 0.91
topics: []
aliases:
  - /v0-91/
status: obsolete
layout: single_special_case
---


<p>
This version, 0.91, is a minor update from version 0.9<br />
A stable version, 1.0, will be published once testing has been completed - this is ongoing and scheduled to be completed at the end of April. 
</p>

<p>
<strong>Changes from version 0.9</strong>
<ul>
    <li><em>dc:creator</em> is now <em>rioxxterms:creator</em></li>
    <li><em>dc:contributor</em> is now <em>rioxxterms:contributor</em></li>
    <li><em>dc:audience</em> is now <em>dcterms:audience</em></li>
</ul>
</p>

<p>
This section details the application profile for RIOXX. The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be interpreted as described in <a href="http://www.ietf.org/rfc/rfc2119.txt">RFC 2119</a>.
</p>

<table border="1" cellspacing="0" cellpadding="0">
<thead>
<tr>
<th valign="top"><b>Element</b></td>
<th valign="top"><b> Cardinality&nbsp;</b></td>
<th valign="top"><b>Description</b></td>
<th valign="top"><b>Roadmap</b></td>
</tr>
</thead>
<tbody>

<tr>
    <td class="nowrap">rioxxterms:creator</td>
    <td class="nowrap">One or more.</td>
    <td>
        <strong>Mandatory</strong><br />
        
The creator of a resource may be a person, organisation or service. Where there is more than one creator, a separate rioxxterms:creator element <strong>MUST</strong> be used for each one.

As many creators may be entered as required. If the creator is a person and it is desired to record that person’s affiliation, the affiliation <strong>SHOULD</strong> be recorded as a rioxxterms:creator element (see rioxxterms:creator).

This element <strong>SHOULD</strong> take an optional attribute called <em>id</em>, designed to hold a machine-readable and unique identifier, if available, for the creator. Any ID entered here <strong>MUST</strong> be in a form which allows it to be parsed and recognised automatically. The ideal use of this element is to include both a machine-readable ID in the <em>id</em> attribute, and a text string in the body of the element, thus:

<pre><code><rioxxterms:creator id=”identifier-for-this-creator-entity”>
    name-of-this-creator-entity
</rioxxterms:creator>```

Where the creator is a person, the <strong>RECOMMENDED</strong> format is to add text in the form Last Name, First Name(s), and to include an ORCID ID, if known, in its HTTP URI form, e.g. 

<pre><code><rioxxterms:creator id=”http://orcid.org/0000-0002-1395-3092”>
    Lawson, Gerald
</rioxxterms:creator>```
    </td>
    <td>
        &nbsp;
    </td>
</tr>


<tr>
    <td class="nowrap">dc:identifier</td>
    <td class="nowrap">Exactly one.</td>
    <td>
        <strong>Mandatory</strong></br>
        
This field <strong>MUST</strong> contain a globally unique and persistent identifier for the resource being described. The identifier <strong>SHOULD</strong> be an HTTP URI that can be de-referenced (and is, thus, actionable). The purpose of this field is to allow access to the resource, therefore it is <strong>RECOMMENDED</strong> that this identifier should point to the actual resource being described by the RIOXX record (typically a PDF file), rather than to an intermediary resource such as a repository web page. This resource <strong>SHOULD</strong> be a version of the resource held in the local repository.
    </td>
    <td>
        &nbsp;
    </td>
</tr>


<tr>
    <td class="nowrap">dc:language</td>
    <td class="nowrap">One or more.</td>
    <td>
        <strong>Mandatory</strong><br />
This refers to the primary language in which the content of the resource is presented. The element <strong>MAY</strong> be repeated if the resource contains multiple languages. Values used for this element <strong>MUST</strong> conform to ISO 639&#8211;3. This offers two and three letter tags e.g. “en” or “eng” for English and “en-GB” for English used in the UK.
    </td>
    <td>
        &nbsp;
    </td>
</tr>


<tr>
    <td class="nowrap">dc:source</td>
    <td class="nowrap">Exactly one.</td>
    <td>
        <strong>Mandatory</strong><br />
The source label describes a resource from which the current resource is derived (in whole or in part). It is <strong>RECOMMENDED</strong> that the source is referenced using a unique identifier from a recognised system e.g. the unique 8-digit International Standard Serial Numbers (ISSN) assigned to print and electronic periodicals.
    </td>
    <td>
        &nbsp;
    </td>
</tr>


<tr>
    <td class="nowrap">dc:title</td>
    <td class="nowrap">Exactly one.</td>
    <td>
        <strong>Mandatory</strong><br />

This refers to the resource’s title and any sub-titles. The title is the form of words by which a resource will be formally known and should be represented using the original spelling and wording. The <strong>RECOMMENDED</strong> format for expressing subtitles is Title:Subtitle

    </td>
    <td>
        &nbsp;
    </td>
</tr>


<tr>
    <td class="nowrap">dcterms:issued</td>
    <td class="nowrap">Exactly one.</td>
    <td>
        <strong>Mandatory</strong><br />

The publication date of the resource. The date <strong>SHOULD</strong> be encoded using ISO 8601 (post&#8211;2004 versions) which follows the following format: YYYY-MM-DD. Year (YYYY) or year and month (YYYY-MM) <strong>MAY</strong> be used if the full date is not known.

    </td>
    <td>
        &nbsp;
    </td>
</tr>


<tr>
    <td class="nowrap">rioxxterms:funder</td>
    <td class="nowrap">One or more.</td>
    <td>
        <strong>Mandatory</strong><br />

The canonical name of the entity responsible for funding the resource being described by this RIOXX record <strong>MUST</strong> be recorded here as text. Where more than one funder exists, each <strong>MUST</strong> be entered as a separate instance of this field.
A controlled list of funder names <strong>SHOULD</strong> be used. A list has been provided for this purpose and is available through the RIOXX web site at <a href="http://docs.rioxx.net/funders/">http://docs.rioxx.net/funders/</a>

    </td>
    <td>
        &nbsp;
    </td>
</tr>


<tr>
    <td class="nowrap">rioxxterms:projectid</td>
    <td class="nowrap">One or more.</td>
    <td>
        <strong>Mandatory</strong><br />

This is designed to collect the project IDs issued by funders that relate to the current resource. It is <strong>REQUIRED</strong> to use the alphanumeric identifier provided by the funder in its original format e.g. ST/K001234/1. Sometimes publications have more than one project ID associated with them; these <strong>MUST</strong> be recorded using separate instances of rioxxterms.projectid. In cases where projects have been funded internally, use whichever internal code is appropriate.

    </td>
    <td>
        &nbsp;
    </td>
</tr>


<tr>
    <td class="nowrap">dc:description</td>
    <td class="nowrap">Zero or more.</td>
    <td>
        <strong>Recommended</strong><br />

This field may be indexed and its contents presented to people conducting searches. The goal is to describe the content of the resource using free text. It is <strong>RECOMMENDED</strong> that an English language abstract be used where available. HTML or other markup tags <strong>SHOULD NOT</strong> be included in this field.

    </td>
    <td>
        &nbsp;
    </td>
</tr>


<tr>
    <td class="nowrap">dc:format</td>
    <td class="nowrap">Zero or one.</td>
    <td>
        <strong>Recommended</strong><br />

This refers to the form of the resource being described in the RIOXX record. The resource can be physical or digital and therefore this element can refer to the media-type or dimensions of that resource.

Where the resource being described is digital, the MIME type of the object pointed to by this RIOXX record’s dc:identifier element <strong>MUST</strong> be entered here.

    </td>
    <td>
        &nbsp;
    </td>
</tr>


<tr>
    <td class="nowrap">dc:publisher</td>
    <td class="nowrap">Zero or more.</td>
    <td>
        <strong>Recommended</strong><br />
        A free text string giving the name of the entity responsible for making the version of record of a resource available. This could be a person, organisation or service.
    </td>
    <td>
        &nbsp;
    </td>
</tr>


<tr>
    <td class="nowrap">dc:rights</td>
    <td class="nowrap">Zero or one</td>
    <td>
        <strong>Recommended</strong><br />

It is <strong>RECOMMENDED</strong> that a URL to an appropriate Creative Commons license is used here, for example: <a href="http://creativecommons.org/licenses/by-sa/3.0/deed.en_GB">http://creativecommons.org/licenses/by-sa/3.0/deed.en_GB</a>

    </td>
    <td>
        Work is under way to develop consensus on a controlled vocabulary that describes rights to open access items as well as the associated issues of Creative Commons licenses and embargo periods. Once this work concludes an expression of rights and licensing is expected to become mandatory.
    </td>
</tr>


<tr>
    <td class="nowrap">dc:subject</td>
    <td class="nowrap">Zero or more.</td>
    <td>
        <strong>Recommended</strong><br />

Normally keywords, phrases or classification codes are used to describe the topic of the resource. If using free text, the use of general keywords <strong>SHOULD</strong> be avoided. It is <strong>RECOMMENDED</strong> to use a formal classification scheme or controlled vocabulary e.g Library of Congress Classification Headings or Medical Subject Headings (MeSH). When including terms from multiple vocabularies, separate element iterations <strong>MUST</strong> be used. If multiple vocabulary terms or keywords are used, terms <strong>SHOULD</strong> be separated with one of the following approaches:

<ul>
<li>the use of semi-colons to separate individual terms</li>
</ul>
or
<ul>
<li>the use of separate iterations of this element for each term.</li>
</ul>

    </td>
    <td>
        &nbsp;
    </td>
</tr>


<tr>
    <td class="nowrap">dcterms:audience</td>
    <td class="nowrap">Zero or more.</td>
    <td>
        <strong>Optional</strong><br />

This field is designed to contain information about the group for which the resource is intended or is considered to be useful. There is no controlled vocabulary for this but sometimes creators or publishers indicate the intended audience. Note that the Research Outcomes System (ROS) used by most of the UK’s Research Councils tracks whether a resource is for a "non-academic audience" (with a drop-down list of possible selections) and whether a resource is for an "international audience". In the absence of alternative formal vocabularies, following the ROS lead is a reasonable course of action.

    </td>
    <td>
        The introduction of a controlled vocabulary for audience will be proposed for phase 2 of the RIOXX project, subject to funding.
    </td>
</tr>


<tr>
    <td class="nowrap">rioxxterms:contributor</td>
    <td class="nowrap">Zero or more.</td>
    <td>
        <strong>Optional</strong><br />

This field is designed to describe an entity – for example the name of a person, organisation or service – responsible for making contributions to the content of the resource. As many rioxxterms:contributor elements may be entered as required. If the contributor is a person and it is desired to record that person's affiliation, the affiliation <strong>MUST</strong> be recorded as a separate rioxxterms:contributor element.

This element <strong>SHOULD</strong> take an optional attribute called <em>id</em>, designed to hold a machine-readable and unique identifier, if available, for the contributor. Any ID entered here <strong>MUST</strong> be in a form which allows it to be parsed and recognised automatically. The ideal use of this element is to include both a machine-readable ID in the <em>id</em> attribute, and a text string in the body of the element, thus:

<pre><code><rioxxterms:contributor id=”identifier-for-this-contributor-entity”>
    name-of-this-contributor-entity
</rioxxterms:contributor>```

Where the contributor is a person, the <strong>RECOMMENDED</strong> format is to add text in the form Last Name, First Name(s), and to include an ORCID ID, if known, in its HTTP URI form, e.g.

<pre><code><rioxxterms:contributor id=”http://orcid.org/0000-0002-1395-3092”>
    Lawson, Gerald
</rioxxterms:contributor>```

    </td>
    <td>
        &nbsp;
    </td>
</tr>


<tr>
    <td class="nowrap">dc:coverage</td>
    <td class="nowrap">Zero or more.</td>
    <td>
        <strong>Optional</strong><br />

This refers to the scope or extent of the content of the resource. It may include jurisdictional, temporal or spatial information. It is <strong>RECOMMENDED</strong> that, where possible, a recognised globally unique identifier is used, such as the Thesaurus of Geographic Names. For example, the place of publication may be recorded.

    </td>
    <td>
        &nbsp;
    </td>
</tr>


<tr>
    <td class="nowrap">dc:type</td>
    <td class="nowrap">Zero or more.</td>
    <td>
        <strong>Optional</strong><br />

Type refers to the nature or genre of the content of the resource and can be entered as free text. Take care not to confuse this with dc:format.

    </td>
    <td>
        The introduction of a controlled vocabulary for 'type' will be proposed for phase 2 of the RIOXX project, subject to funding.
    </td>
</tr>


<tr>
    <td class="nowrap">dc.relation</td>
    <td class="nowrap">Zero or more.</td>
    <td>
        <strong>Optional</strong><br />

This format of this element <strong>SHOULD</strong> be an HTTP URI which points to a related resource.
It is <strong>RECOMMENDED</strong> that, where available, the publisher’s DOI for the main resource being described in the RIOXX record also be entered here, in it’s HTTP form – e.g. http://dx.doi.org/10.1006/jmbi.1995.0238

Each related resource <strong>MUST</strong> appear as a separate instance of the field.

    </td>
    <td>
        &nbsp;
    </td>
</tr>


<tr>
    <td class="nowrap">dcterms:references</td>
    <td class="nowrap">Zero or more.</td>
    <td>
        <strong>Optional</strong></br />

The format of this element <strong>SHOULD</strong> be an HTTP URI which points to a resource referenced by the resource described in the RIOXX record. Common examples might include a data-set which underpins a paper being described in the record.

Each reference <strong>MUST</strong> appear as a separate instance of this element.

    </td>
    <td>
        &nbsp;
    </td>
</tr>



</tbody>
</table>
