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

#### [Version 3.0 RC 1 (DRAFT)](/profiles/v3-0-rc-1/)
###### Changes since [Version 2.0 Final Release:](https://www.rioxx.net/profiles/v2-0-final/)
- Separation of project and grant data, with the creation of `<rioxxterms:grants>` alongside `<rioxxterms:project>`
- Wider support for persistent identifier (PID) schemes across `<rioxxterms:author>`, `<rioxxterms:contributor>`, `<rioxxterms:project>` and `<dc:publisher>`, with an increased range of PID schemes recommended to reflect growing maturity in the PID landscape
- Updates to the usage of RFC 2119 terminology throughout the profile
- General improvements to language used in profile documentation
- The name of the 'RIOXX Metadata Application Profile' changed to 'Rioxx: Research Outputs Metadata Schema' to better communicate its purpose
- `<ali:license_ref>`, `<rioxxterms:author>`, `<rioxxterms:contributor>`, `<rioxxterms:project>`, `<rioxxterms:version_of_record>` **updated** to explicitly note HTTPS use where URI values are specified.
- **Removed** the `<ali:free_to_read>` property.
- **Removed** the `<rioxxterms:apc>` property.
- Addition of the a **new** property: `<rioxxterms:record_public_release_date>` encoded according to ISO8601/W3CDTF.
- `<rioxxterms:publication_date>` **updated** to specify encoding as per ISO8601/W3CDTF, including resources with seasonal publication dates.
- Controlled list of types in  `<rioxxterms:type>` **removed** and **updated** to specify the [COAR Controlled Vocabulary Resource Type Genres](http://vocabularies.coar-repositories.org/documentation/resource_types/).
- **Major change** to the use of `<dc:identifier>` to accommodate multiple 'expressions' of the same 'work'. In particular, introduction of  `<dc:relation>` and the parallel use of the 'uri', 'deposit_date', 'resource_exposed_date' and 'type' attributes. The 'type' attribute makes use of [schema.org](https://schema.org/) [vocabulary definitions]().
- General move away from using the XML 'id' attribute across RIOXX to uniquely identify element content using URI(s) and the introduction of the 'uri' attribute. This change specifically affects `<rioxxterms:author>`, `<rioxxterms:contributor>`, `<rioxxterms:publisher>` and `<rioxxterms:type>`.



#### [Version 2.0 Final](/profiles/v2-0-final/)

This is an updated version of the RIOXX application profile, enhanced following the outcomes of the [V4OA](http://www.v4oa.net) project.

###### Changes since version 1.0

* changed <dcterms:dateAccepted> to only allow YYYY-MM-DD and not YYYY-MM
* changed <dcterms:dateAccepted> to only allow YYYY-MM and not YYYY
* very slight change to wording in <dc:identifier>
* recommendation to use ISBN13 rather than book title in dc:source
* removed description of dc:subject and pointed to OpenAIRE guidelines
* added the ali namespace prefix to <license_ref> and <free_to_read>
* added recommendation to use ISNI for identification of funders, as well as for authors and contributors where these are organisations
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