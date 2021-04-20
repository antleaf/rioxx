---
title: Profiles
date: '2018-05-16'
description: ''
draft: false
tags: []
notes: ''
aliases:
- "/release_notes/"
layout: profiles_list
---



#### [Version 2.0 Final Release](/profiles/v2-0-final/)

###### Changes since version 2.0 RC 2

* changed &lt;dcterms:dateAccepted&gt; to only allow YYYY-MM-DD and not YYYY-MM

#### [Version 2.0 RC 2](/profiles/v2-0-rc-2/)

###### Changes since version 2.0 beta 1

* changed &lt;dcterms:dateAccepted&gt; to only allow YYYY-MM and not YYYY
* very slight change to wording in &lt;dc:identifier&gt;
* recommendation to use ISBN13 rather than book title in dc:source
* removed description of dc:subject and pointed to OpenAIRE guidelines
* added the ali namespace prefix to &lt;license_ref&gt; and &lt;free_to_read&gt;
* added recommendation to use ISNI for identification of funders, as well as for authors and contributors where these are organisations

#### [Version 2.0 beta 1](/profiles/v2-0-beta-1/)

This is an updated version of the RIOXX application profile, enhanced following the outcomes of the [V4OA](http://www.v4oa.net) project.

###### Changes since version 1.0

* the &lt;free_to_read&gt; element has been added
* the &lt;license_ref&gt; element has been added
* the &lt;dc:rights&gt; element has been removed - the introduction of the new &lt;license_ref&gt; has superseded this
* the recommendations for the &lt;rioxxterms:funder&gt; element have changed - the use of [FundRef](http://www.crossref.org/fundref/) is now recommended.
* the &lt;rioxxterms:apc&gt; element has been added
* the &lt;rioxxterms:version&gt; element has been added
* the &lt;rioxxterms:creator&gt; element has been replaced with &lt;rioxxterms:author&gt;
* the new &lt;rioxxterms:project&gt; element has replaced both &lt;rioxxterms:projectid&gt; and &lt;rioxxterms:funder&gt;
* the &lt;rioxxterms:version_of_record&gt; element has been added, and the recommendation to include, under &lt;dc:relation&gt;, the DOI to the version of record has been removed.
* the &lt;dcterms:issued&gt; element has been replaced with the &lt;dcterms:dateAccepted&gt;.
* the &lt;dc:type&gt; element has been replaced with the &lt;rioxxterms:type&gt; and this element has been constrained with a controlled list of allowed values.
* the &lt;dcterms:audience&gt; element has been removed.
* the &lt;dcterms:references&gt; element has been removed.
* &lt;rioxxterms:publication_date&gt; has been added

#### [Version 1.0](/profiles/v1-0/)
This is the initial release of the RIOXX application profile