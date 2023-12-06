---
title: Profiles
date: '2023-11-15'
description: ''
draft: false
tags: []
notes: ''
aliases:
- "/release_notes/"
layout: profiles_list
---

#### [Version 3.0](/profiles/v3-0-final/)
###### Changes since [Version 2.0 Final Release:](/profiles/v2-0-final/)
- Separation of project and grant data, with the creation of **new** properties: `<rioxxterms:grant>` and `<rioxxterms:project>`.
- Creation of **new** sub-properties `<rioxxterms:name>` and `<rioxxterms:id>`, to be used in conjunction with `<rioxxterms:creator>` (updated from `<rioxxterms:author>` in Version 2.0) and `<rioxxterms:contributor>`.
- Creation of a **new** property: `<rioxxterms:record_public_release_date>` encoded according to ISO8601/W3CDTF.
- Creation of the **new** property `<rioxxterms:ext_relation>`, used to convey external associations to related scholarly entities. Such relational associations will be scholarly entities hosted externally or outsider the direct custodianship of the repository.
- `<rioxxterms:creator>`, `<rioxxterms:contributor>`, `<rioxxterms:project>` and `<dc:publisher>` **updated** to better support persistent identifier (PID) schemes. An increased range of PID schemes recommended, to reflect growing maturity in the PID landscape.
- `<rioxxterms:publication_date>` **updated** to specify encoding as per ISO8601/W3CDTF, including resources with seasonal publication dates.
- Type property **updated** from `<rioxxterms:type>` to `<dc:type>`, and updated to specify the [COAR Controlled Vocabulary Resource Type Genres](http://vocabularies.coar-repositories.org/documentation/resource_types/).
- Properties **updated** throughout schema to explicitly specify use of HTTPS URIs. 
- Usage of RFC 2119 terminology **updated** throughout the schema.
- **Removed** the `<ali:free_to_read>` property.
- **Removed** the `<rioxxterms:apc>` property.
- **Removed** the `<rioxxterms:version_of_record>` property, superseded by updates to attribute usage within the `<dc:relation>` and `<rioxxterms:ext_relation>` properties.
- **Major change** to the use of `<dc:identifier>` to accommodate an HTTP(S) URI identifying the resource, resolving to a repository 'landing page' which describes the resource. 
- **Major change** to the use of `<dc:relation>`, with the introduction of the following associated attributes: `rel`, `type`, `coar_type`, `coar_version`, `deposit_date`, `resource_exposed_date`, `access_rights`, and `license_ref`. `<dc:relation>` to be used as principal mechanism for expressing the existence of harvestable file content, as well as other internally curated resources. To be considered in conjunction with the **new** property, `<rioxxterms:ext_relation>`.
- General move away from using the XML 'id' attribute across Rioxx to uniquely identify element content using URI(s) and the introduction of the 'uri' attribute. 
- General improvements to language used in schema documentation
- The name of the 'RIOXX Metadata Application Profile' changed to 'Rioxx: Research Outputs Metadata Schema' to better communicate its purpose

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
