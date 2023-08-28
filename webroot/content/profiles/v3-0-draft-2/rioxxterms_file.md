---
date: '2023-05-06T16:04:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:file
cardinality: Zero or more
requirement: Should
metadata_profile: v3-0-rc-2
---

Although this property is not strictly mandated in the Rioxx application profile, it **SHOULD** be included because this is the property which harvesting software will inspect to locate URLs for resource file content - for example to locate the "full text" associated with a repository record.

The `rioxxterms:file` property identifies a downloadable resource. Each `rioxxterms:file` property **MUST** contain an HTTP(S) URI resolving to the downloadable resource. 

`rioxxterms:file` is further refined by a series of attributes, which **SHOULD** be included (where applicable): 

* `coar_type`
* `coar_version`
* `deposit_date`
* `resource_exposed_date`
* `cite_as`
* `access_rights`
* `license_ref`
* `format`

### Attributes

1. *coar_type*:  When used, the `coar_type` attribute **MUST** contain a value which is an identifier from the [COAR Resource Types Vocabulary](http://purl.org/coar/resource_type/). For example, for the common case of the related resource being a PDF of a journal article, the **RECOMMENDED** value would be `http://purl.org/coar/resource_type/c_6501`. The [COAR Resource Types Vocabulary](http://purl.org/coar/resource_type/) accommodates a diverse range of resource types. `rioxxterms:file` can therefore also be used to communicate the existence of harvestable related data or software, such as by types [experimental data](http://purl.org/coar/resource_type/63NG-B465) or [research software](http://purl.org/coar/resource_type/c_c950).
2. *coar_version*: When used, the `coar_version` attribute **MUST** contain a value which is an identifier from the [COAR Version Types Vocabulary](http://purl.org/coar/version/).
3. *deposit_date*: The `deposit_date` attribute (if present) takes the date on which this resource was first deposited, irrespective of any relevant embargoes or dark archiving, and irrespective of any subsequent file replacement(s). It is anticipated that in some circumstances the `deposit_date` will be captured and exposed in repository metadata when the resource described is under temporary embargo or temporary dark archiving. If included, this attribute's value **MUST** be encoded according to the [W3CDTF](https://www.w3.org/TR/NOTE-datetime) (a profile of [ISO 8601](https://www.iso.org/standard/40874.html)) which typically follows the following format: YYYY-MM-DD.
4. *resource_exposed_date*: The `resource_exposed_date` attribute (if present) takes the date on which this related resource was made publicly available, irrespective of any subsequent file replacement(s). If included, this attribute's value **MUST** be encoded according to the [W3CDTF](https://www.w3.org/TR/NOTE-datetime) (a profile of [ISO 8601](https://www.iso.org/standard/40874.html)) which typically follows the following format: YYYY-MM-DD. Repositories will typically fulfil `resource_exposed_date` if the related resource is made publicly visible immediately upon deposit, or when an applicable embargo ends.
5. *cite_as*: When used, the `cite_as` attribute **MUST** communicate the HTTP(S) URI which identifies the value of `rioxxterms:file`. `cite_as` is likely to be populated by a persistent identifier (PID) that resolves to a repository 'landing page', as per good practice. Possible values here may include a DOI, URN, CORE OAI ID; or a repository URL where there is no requirement for a PID.
6. *access_rights*: When used, the `access_rights` attribute **MUST** take a URI value from the [COAR Access Rights Vocabulary](https://vocabularies.coar-repositories.org/access_rights/), which defines four access states: [embargoed access](http://purl.org/coar/access_right/c_f1cf), [metadata only access](http://purl.org/coar/access_right/c_14cb), [open access](http://purl.org/coar/access_right/c_abf2), [restricted access](http://purl.org/coar/access_right/c_16ec).
7. *license_ref*: When used, the `license_ref` attribute **MUST** communicate the license terms under which the value of `rioxxterms:file` is subject using an HTTP(S) URI. Typical examples might include the variety of licenses made available by Creative Commons, but can conceivably include any license referencible by URI.
8. *format*: The final attribute, `format`, refers to the technical format of the value of `rioxxterms:file`. When used, `format` **MUST** encode the [Media Type](https://www.iana.org/assignments/media-types/media-types.xhtml) of the resource (formerly MIME Type). Note that this element should not be confused with `rioxxterms:type`.

### Examples

**Example 1:**

A typical `rioxxterms:file` property may resemble this example, in which the property value is the downloadable resource and the `cite_as` attribute communicates its local DOI:

```xml
<rioxxterms:file coar_type="https://purl.org/coar/resource_type/c_6501" coar_version="https://purl.org/coar/version/c_ab4af688f83e57aa"
    deposit_date="2023-03-28" 
    resource_exposed_date="2023-03-28" 
    cite_as="https://doi.org/10.17868/strath.00084907"
    access_rights="https://purl.org/coar/access_right/c_abf2"
    license_ref="https://creativecommons.org/licenses/by/4.0/"
    format="application/pdf">
            https://strathprints.strath.ac.uk/84907/7/Jiang_etal_IEEETGRS_2023_Microseismic_event_classification.pdf
</rioxxterms:file>
```

**Example 2**

The following example is similar to Example 1 but uses Handle.net instead of a DOI:

```xml
<rioxxterms:file coar_type="https://purl.org/coar/resource_type/c_6501" coar_version="https://purl.org/coar/version/c_ab4af688f83e57aa"
    deposit_date="2010-01-20" 
    resource_exposed_date="2020-01-20"     
    access_rights="https://purl.org/coar/access_right/c_abf2"
    cite_as="https://hdl.handle.net/10044/1/76123"
    license_ref="https://creativecommons.org/licenses/by-nc-nd/4.0"
	format="application/pdf">https://spiral.imperial.ac.uk/bitstream/10044/1/76123/2/POP19-AR-58732_accepted.pdf
</rioxxterms:file>  
```

