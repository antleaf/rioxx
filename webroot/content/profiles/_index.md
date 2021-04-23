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

* changed <dcterms:dateAccepted> to only allow YYYY-MM-DD and not YYYY-MM

#### [Version 2.0 RC 2](/profiles/v2-0-rc-2/)

###### Changes since version 2.0 beta 1

* changed <dcterms:dateAccepted> to only allow YYYY-MM and not YYYY
* very slight change to wording in <dc:identifier>
* recommendation to use ISBN13 rather than book title in dc:source
* removed description of dc:subject and pointed to OpenAIRE guidelines
* added the ali namespace prefix to <license_ref> and <free_to_read>
* added recommendation to use ISNI for identification of funders, as well as for authors and contributors where these are organisations

#### [Version 2.0 beta 1](/profiles/v2-0-beta-1/)

This is an updated version of the RIOXX application profile, enhanced following the outcomes of the [V4OA](http://www.v4oa.net) project.

###### Changes since version 1.0

* the <free_to_read> element has been added
* the <license_ref> element has been added
* the <dc:rights> element has been removed - the introduction of the new <license_ref> has superseded this
* the recommendations for the <rioxxterms:funder> element have changed - the use of [FundRef](http://www.crossref.org/fundref/) is now recommended.
* the <rioxxterms:apc> element has been added
* the <rioxxterms:version> element has been added
* the <rioxxterms:creator> element has been replaced with <rioxxterms:author>
* the new <rioxxterms:project> element has replaced both <rioxxterms:projectid> and <rioxxterms:funder>
* the <rioxxterms:version_of_record> element has been added, and the recommendation to include, under <dc:relation>, the DOI to the version of record has been removed.
* the <dcterms:issued> element has been replaced with the <dcterms:dateAccepted>.
* the <dc:type> element has been replaced with the <rioxxterms:type> and this element has been constrained with a controlled list of allowed values.
* the <dcterms:audience> element has been removed.
* the <dcterms:references> element has been removed.
* <rioxxterms:publication_date> has been added

#### [Version 1.0](/profiles/v1-0/)
This is the initial release of the RIOXX application profile