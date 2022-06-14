---
date: '2022-06-13T11:00:43+00:00'
draft: false
type: metadata_profile_property
title: dc:relation
cardinality: Zero or more
requirement: Should
metadata_profile: v3-0-rc-1
---

Although this property is not strictly mandated in the RIOXX application profile, it **SHOULD** be included because this is the property which harvesting software will inspect for resource file content - for example to locate the "full text" associated with a repository record.

The *resource* described by a RIOXX record is commonly a web page containing metadata and links to other resources, such as (in the case of a publication) a PDF file. The `dc:relation` property identifies these other, related resources. Each `dc:relation` property **MUST** contain an HTTP(S) URI, and **MUST** include the following attributes: 

* `type`
* `deposit_date`
* `resource_exposed_date`

The `type` attribute must contain a value which is an identifier from the [schema.org vocabulary](https://schema.org/docs/developers.html#defs). For example, for the common case of the related resource being a PDF of a journal article, then the recommended value would be `https://schema.org/ScholarlyArticle`

The `deposit_date` attribute takes the date on which this related resource was first deposited, irrespective of any relevant embargoes or dark archiving, and irrespective of any subsequent file replacement(s). It is anticipated that in some circumstances the `deposit_date` will be captured and exposed in repository metadata when the resource described is under temporary embargo or temporary dark archiving. This attribute's value **MUST** be encoded according to the [W3CDTF](https://www.w3.org/TR/NOTE-datetime) (a profile of [ISO 8601](https://www.iso.org/standard/40874.html)) which typically follows the following format: YYYY-MM-DD.

The `resource_exposed_date` attribute takes the date on which this related resource was made publicly available, irrespective of any subsequent file replacement(s). This attribute's value **MUST** be encoded according to the [W3CDTF](https://www.w3.org/TR/NOTE-datetime) (a profile of [ISO 8601](https://www.iso.org/standard/40874.html)) which typically follows the following format: YYYY-MM-DD. Repositories will typically fulfil `resource_exposed_date` if the related resource is made publicly visible immediately upon deposit, or when an applicable embargo ends.

Each related resource **MUST** appear as a separate instance of the element.

(Note that the persistent identifier for the 'version of record' is not recorded here but **MUST** be recorded in the *rioxxterms:version_of_record* element. If the file associated with the 'version of record' is a deposit then its file location can be encoded here)

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
The [schema.org](https://schema.org/) vocabulary accommodates a diverse range of [creative work types](https://schema.org/CreativeWork).  `dc:relation` can therefore also be used to communicate the existence of related data or software, such as by types [DataSet](https://schema.org/DataSet) or [SoftwareSourceCode](https://schema.org/SoftwareSourceCode). Where such types have been encoded it will be considered to be for the purposes of contributing to the scholarly data graph rather than for assisting harvesting software in locating file content, such as full-text. The `version` attribute is **OPTIONAL**

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