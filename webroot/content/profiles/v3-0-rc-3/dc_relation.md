---
date: '2023-05-06T16:04:43+00:00'
draft: false
type: metadata_profile_property
title: dc:relation
cardinality: Zero or more
requirement: Should
metadata_profile: v3-0-rc-3
---

Although this property is not strictly mandated in the Rioxx application profile, it **SHOULD** be included because this is the property which harvesting software will inspect to locate URLs for resource file content - for example to locate the "full text" associated with a repository record.

The `dc:relation` property identifies a <mark>downloadable</mark> resource. Each `dc:relation` property **MUST** contain an HTTP(S) URI resolving to the downloadable resource. 

`dc:relation` is further refined by a series of attributes, which **SHOULD** be included (where applicable): 

* `rel`
* `coar_type`
* `coar_version`
* `deposit_date`
* `resource_exposed_date`
* `cite-as`
* `access_rights`
* `license_ref`
* `type`

### Attributes
1. *rel*: <mark>needs definition</mark>
1. *coar_type*:  When used, the `coar_type` attribute **MUST** contain a value which is an identifier from the [COAR Resource Types Vocabulary](http://purl.org/coar/resource_type/). For example, for the common case of the related resource being a PDF of a journal article, the **RECOMMENDED** value would be `http://purl.org/coar/resource_type/c_6501`. The [COAR Resource Types Vocabulary](http://purl.org/coar/resource_type/) accommodates a diverse range of resource types. `dc:relation` can therefore also be used to communicate the existence of harvestable related data or software, such as by types [experimental data](http://purl.org/coar/resource_type/63NG-B465) or [research software](http://purl.org/coar/resource_type/c_c950).
2. *coar_version*: When used, the `coar_version` attribute **MUST** contain a value which is an identifier from the [COAR Version Types Vocabulary](http://purl.org/coar/version/).
3. *deposit_date*: The `deposit_date` attribute (if present) takes the date on which this resource was first deposited, irrespective of any relevant embargoes or dark archiving, and irrespective of any subsequent file replacement(s). It is anticipated that in some circumstances the `deposit_date` will be captured and exposed in repository metadata when the resource described is under temporary embargo or temporary dark archiving. If included, this attribute's value **MUST** be encoded according to the [W3CDTF](https://www.w3.org/TR/NOTE-datetime) (a profile of [ISO 8601](https://www.iso.org/standard/40874.html)) which typically follows the following format: YYYY-MM-DD.
4. *resource_exposed_date*: The `resource_exposed_date` attribute (if present) takes the date on which this related resource was made publicly available, irrespective of any subsequent file replacement(s). If included, this attribute's value **MUST** be encoded according to the [W3CDTF](https://www.w3.org/TR/NOTE-datetime) (a profile of [ISO 8601](https://www.iso.org/standard/40874.html)) which typically follows the following format: YYYY-MM-DD. Repositories will typically fulfil `resource_exposed_date` if the related resource is made publicly visible immediately upon deposit, or when an applicable embargo ends.
5. *cite-as*: <mark>needs definition</mark>
6. *access_rights*: When used, the `access_rights` attribute **MUST** take a URI value from the [COAR Access Rights Vocabulary](https://vocabularies.coar-repositories.org/access_rights/), which defines four access states: [embargoed access](http://purl.org/coar/access_right/c_f1cf), [metadata only access](http://purl.org/coar/access_right/c_14cb), [open access](http://purl.org/coar/access_right/c_abf2), [restricted access](http://purl.org/coar/access_right/c_16ec).
7. *license_ref*: When used, the `license_ref` attribute **MUST** communicate the license terms under which the value of `dc:relation` is subject using an HTTP(S) URI. Typical examples might include the variety of licenses made available by Creative Commons, but can conceivably include any license referencible by URI.
8. *type*: The final attribute, `format`, refers to the technical format of the value of `dc:relation`. When used, `format` **MUST** encode the [Media Type](https://www.iana.org/assignments/media-types/media-types.xhtml) of the resource (formerly MIME Type). Note that this element should not be confused with `rioxxterms:type`.

### Examples

**Example 1:**

<mark>describe this example</mark>

```xml
<dc:relation
        rel="item"
        type="application/pdf"
        coar_version="https://purl.org/coar/version/c_ab4af688f83e57aa"
        coar_type="https://vocabularies.coar-repositories.org/resource_types/c_6501/"
        deposit_date="2019-12-11"
        resource_exposed_date="2019-12-11"
        access_rights_="https://purl.org/coar/access_right/c_abf2"
        license_ref="https://creativecommons.org/licenses/by-nc-nd/4.0/">
    https://strathprints.strath.ac.uk/70117/7/Wilson_Heath_OS2019_Increasing_turbidity_in_the_North_Sea_during_the_20th_century.pdf
</dc:relation>
```

**Example 2**

<mark>describe this example</mark>

```xml
<dc:relation
        rel="cite-as">
    https://oai.core.ac.uk/oai:strathprints.strath.ac.uk:70117
</dc:relation>  
```

