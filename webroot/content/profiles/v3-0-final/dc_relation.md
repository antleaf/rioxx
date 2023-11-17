---
date: '2023-10-23T16:04:43+00:00'
draft: false
type: metadata_profile_property
title: dc:relation
cardinality: Zero or more
requirement: Should
metadata_profile: v3-0-final
---

Although this property is not strictly mandated in the Rioxx application profile, it **SHOULD** be included because this is the property which harvesting software will inspect to locate URLs for resource file content - for example to locate the "full text" associated with a repository record. It will also be the property to declare a persistent identifier (PID) that may be associated with the resource. 

Note that only those resources under the direct custodianship of the repository should be asserted within `dc:relation`. Entities outside the custodianship of the repository should be related using `rioxxterms:ext_relation`. 
 
`dc:relation` is refined by a series of attributes, which **SHOULD** be included (where applicable): 

* `rel`
* `type`
* `coar_type`
* `coar_version`
* `deposit_date`
* `resource_exposed_date`
* `access_rights`
* `license_ref`

When set to `rel="item"`, the `dc:relation` property identifies a downloadable resource. Each such `dc:relation` property **MUST** contain an HTTP(S) URI resolving to the downloadable resource. It is **REQUIRED** that this property is used whenever the Rioxx record identifies a downloadable object under the direct custodianship of the repository, such as a full text, dataset or software. Where such deposited downloadable resource remains under a temporary embargo, the repository **SHOULD** return HTTP status code 451 Unavailable For Legal Reasons until the embargo's expiry. 

When set to `rel="cite-as"`, the `dc:relation` property specifies a persistent identifier associated with the resource. `dc:relation` shall only be used to convey PIDs identifying resources under the direct custodianship of the repository, therefore all PIDs specified under `dc:relation` **MUST** resolve to the repository. PIDs identifying related resources that resolve to resources outside of the direct custodianship of the repository will be specified under `rioxterms:ext_relation`. 

The `dc:relation` property can be repeated to specify more than one persistent identifier associated with the resource. Possible values here may include a DOI, URN, CORE OAI ID; or an alternative repository HTTP(S) URI where there is no requirement for a PID. ### Attributes

1. *rel*: The `rel` attribute uses 'typed links' from the [IANA Link Relation Registry](https://www.iana.org/assignments/link-relations/link-relations.xhtml). This attribute will often be set to `rel='item'` where `dc:relation` is being used to communicate downloadable file content, but will be set to `rel="cite-as"` where `dc:relation` is simulataneously being used to declare an associated persistent identifier.
2. *type*: The `type` attribute refers to the technical format of the value of `dc:relation`. When used, `type` **MUST** encode the [Media Type](https://www.iana.org/assignments/media-types/media-types.xhtml) of the resource (formerly MIME Type). Note that this attribute should not be confused with `coar_type`.
3. *coar_type*:  When used, the `coar_type` attribute **MUST** contain a value which is an identifier from the [COAR Resource Types Vocabulary](http://purl.org/coar/resource_type/). For example, for the common case of the resource being a PDF of a journal article, the **RECOMMENDED** value would be `http://purl.org/coar/resource_type/c_6501` ('journal article'). The [COAR Resource Types Vocabulary](http://purl.org/coar/resource_type/) accommodates a diverse range of resource types. `dc:relation` can therefore also be used to communicate the existence of directly harvestable related data or software, such as by types [experimental data](http://purl.org/coar/resource_type/63NG-B465) or [research software](http://purl.org/coar/resource_type/c_c950).
2. *coar_version*: When used, the `coar_version` attribute **MUST** contain a value which is an identifier from the [COAR Version Types Vocabulary](http://purl.org/coar/version/).
3. *deposit_date*: The `deposit_date` attribute (if present) takes the date on which this resource was first deposited, irrespective of any relevant embargoes or dark archiving, and irrespective of any subsequent file replacement(s). It is anticipated that in some circumstances the `deposit_date` will be captured and exposed in repository metadata when the resource described is under temporary embargo or temporary dark archiving. If included, this attribute's value **MUST** be encoded according to the [W3CDTF](https://www.w3.org/TR/NOTE-datetime) (a profile of [ISO 8601](https://www.iso.org/standard/40874.html)) which typically follows the following format: YYYY-MM-DD.
4. *resource_exposed_date*: The `resource_exposed_date` attribute (if present) takes the date on which this related resource was made publicly available, irrespective of any subsequent file replacement(s). If included, this attribute's value **MUST** be encoded according to the [W3CDTF](https://www.w3.org/TR/NOTE-datetime) (a profile of [ISO 8601](https://www.iso.org/standard/40874.html)) which typically follows the following format: YYYY-MM-DD. Repositories will typically fulfil `resource_exposed_date` if the related resource is made publicly visible immediately upon deposit, or when an applicable embargo ends.
6. *access_rights*: When used, the `access_rights` attribute **MUST** take a URI value from the [COAR Access Rights Vocabulary](https://vocabularies.coar-repositories.org/access_rights/), which defines four access states: [embargoed access](http://purl.org/coar/access_right/c_f1cf), [metadata only access](http://purl.org/coar/access_right/c_14cb), [open access](http://purl.org/coar/access_right/c_abf2), [restricted access](http://purl.org/coar/access_right/c_16ec).
7. *license_ref*: When used, the `license_ref` attribute **MUST** communicate the license terms under which the value of `rioxxterms:file` is subject using an HTTP(S) URI. Typical examples might include the variety of licenses made available by Creative Commons, but can conceivably include any license referencible by URI.

### Examples

**Example 1:**

A typical `dc:relation` property may resemble this example, in which the property value is the downloadable resource:

```xml
<dc:relation 
    rel="item"
    type="application/pdf"
    coar_type="https://purl.org/coar/resource_type/c_6501" 
    coar_version="https://purl.org/coar/version/c_ab4af688f83e57aa"
    deposit_date="2023-03-28" 
    resource_exposed_date="2023-03-28" 
    access_rights="https://purl.org/coar/access_right/c_abf2"
    license_ref="https://creativecommons.org/licenses/by/4.0/">
            https://strathprints.strath.ac.uk/84907/7/Jiang_etal_IEEETGRS_2023_Microseismic_event_classification.pdf
</dc:relation>
```

**Example 2:**

Example 1 can be elaborated to declare the local repository PID associated with the downloadable resource, in this case a DOI:

```xml
<dc:relation 
    rel="item"
    type="application/pdf"
    coar_type="https://purl.org/coar/resource_type/c_6501" 
    coar_version="https://purl.org/coar/version/c_ab4af688f83e57aa"
    deposit_date="2023-03-28" 
    resource_exposed_date="2023-04-11" 
    access_rights="https://purl.org/coar/access_right/c_abf2"
    license_ref="https://creativecommons.org/licenses/by/4.0/">
            https://strathprints.strath.ac.uk/84907/7/Jiang_etal_IEEETGRS_2023_Microseismic_event_classification.pdf
</dc:relation>

<dc:relation rel="cite-as">https://doi.org/10.17868/strath.00084907</dc:relation>
             
```

**Example 3:**

The `dc:relation` property can be repeated to communicate the existence of more than one downloadable resource. This example also includes the declaration of a repository PID associated with resources. 

```xml
<dc:relation 
    rel="item"
    type="application/pdf"
    coar_type="https://purl.org/coar/resource_type/c_6501" 
    coar_version="https://purl.org/coar/version/c_970fb48d4fbd8a85"
    deposit_date="2023-10-18" 
    resource_exposed_date="2023-10-18" 
    access_rights="https://purl.org/coar/access_right/c_abf2"
    license_ref="https://creativecommons.org/licenses/by/4.0/">
            https://eprints.whiterose.ac.uk/204315/1/amt-16-4375-2023.pdf
</dc:relation>

<dc:relation 
    rel="item"
    type="application/pdf"
    coar_type="http://purl.org/coar/resource_type/YZ1N-ZFT9" 
    deposit_date="2023-10-18" 
    resource_exposed_date="2023-10-18" 
    access_rights="https://purl.org/coar/access_right/c_abf2"
    license_ref="https://creativecommons.org/licenses/by/4.0/">
             https://eprints.whiterose.ac.uk/204315/9/amt-16-4375-2023-supplement.pdf
</dc:relation>

<dc:relation rel="cite-as">https://oai.core.ac.uk/oai:eprints.whiterose.ac.uk:204315</dc:relation>
             
```
