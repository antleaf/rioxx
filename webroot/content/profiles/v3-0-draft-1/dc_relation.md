---
date: '2022-06-17T16:04:43+00:00'
draft: false
type: metadata_profile_property
title: dc:relation
cardinality: Zero or more
requirement: Should
metadata_profile: v3-0-rc-1
---

Although this property is not strictly mandated in the Rioxx application profile, it **SHOULD** be included because this is the property which harvesting software will inspect for to find the URLs for resource file content - for example to locate the "full text" associated with a repository record.

The *resource* described by a Rioxx record is commonly a web page containing metadata and links to other resources, such as (in the case of a publication) a PDF file. The `dc:relation` property identifies these other, related resources. Each `dc:relation` property **MUST** contain an HTTP(S) URI, and **SHOULD** include the following attributes: 

* `type`
* `deposit_date`
* `resource_exposed_date`

The `type` attribute (if present) **MUST** contain a value which is an identifier from the [schema.org vocabulary](https://schema.org/docs/developers.html#defs). For example, for the common case of the related resource being a PDF of a journal article, then the **RECOMMENDED** value would be `https://schema.org/ScholarlyArticle`

The `deposit_date` attribute (if present) takes the date on which this related resource was first deposited, irrespective of any relevant embargoes or dark archiving, and irrespective of any subsequent file replacement(s). It is anticipated that in some circumstances the `deposit_date` will be captured and exposed in repository metadata when the resource described is under temporary embargo or temporary dark archiving. If included, this attribute's value **MUST** be encoded according to the [W3CDTF](https://www.w3.org/TR/NOTE-datetime) (a profile of [ISO 8601](https://www.iso.org/standard/40874.html)) which typically follows the following format: YYYY-MM-DD.

The `resource_exposed_date` attribute (if present) takes the date on which this related resource was made publicly available, irrespective of any subsequent file replacement(s). If included, this attribute's value **MUST** be encoded according to the [W3CDTF](https://www.w3.org/TR/NOTE-datetime) (a profile of [ISO 8601](https://www.iso.org/standard/40874.html)) which typically follows the following format: YYYY-MM-DD. Repositories will typically fulfil `resource_exposed_date` if the related resource is made publicly visible immediately upon deposit, or when an applicable embargo ends.

Each related resource **MUST** appear as a separate instance of the property.

Example:
```xml
<dc:relation type="https://schema.org/ScholarlyArticle" deposit_date="2021-07-06" resource_exposed_date="2021-07-20">
    https://www.repository.org/article_123456_preprint.pdf
</dc:relation>

<dc:relation type="https://schema.org/ScholarlyArticle" deposit_date="2021-07-28" resource_exposed_date="2021-07-28">
    https://www.repository.org/article_1234567.pdf
</dc:relation>

<dc:relation type="https://schema.org/ScholarlyArticle" deposit_date="2022-03-14" resource_exposed_date="2022-03-14">
    https://www.repository.org/article_1234567_JATS.xml
</dc:relation>
```
The [schema.org](https://schema.org/) vocabulary accommodates a diverse range of [creative work types](https://schema.org/CreativeWork).  `dc:relation` can therefore also be used to communicate the existence of related data or software, such as by types [DataSet](https://schema.org/Dataset) or [SoftwareSourceCode](https://schema.org/SoftwareSourceCode). These examples are suggested in the interest of contributing to the scholarly data graph in general.

Examples:
```xml
<dc:relation type="https://schema.org/DataSet" deposit_date="2022-01-13" resource_exposed_date="2022-01-20">
    https://doi.org/10.5281/zenodo.3538919
</dc:relation>
```

```xml
<dc:relation type="https://schema.org/SoftwareSourceCode" deposit_date="2022-03-23" resource_exposed_date="2022-04-18">
    https://github.com/covid19datahub/R
</dc:relation>
```
