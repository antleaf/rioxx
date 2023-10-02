---
date: '2023-06-01T16:04:43+00:00'
draft: false
type: metadata_profile_property
title: "rioxxterms:ext_relation"
cardinality: Zero or more
requirement: Should
metadata_profile: v3-0-rc-3
---

`rioxxterms:ext_relation` is used to convey associations to related scholarly entities. This will typically include alternative 'expressions' of *the resource* (e.g. preprint, VoR, etc.) and/or entities relevant to understanding *the resource*, such as related research data, software, instruments, and so forth. Where such types have been encoded it will be considered to be for the purposes of contributing to the scholarly data graph rather than for assisting harvesting software in locating file content, such as full-text, which is instead enabled via `dc:relation` property.

Each relation **MUST** appear as a separate instance of the `rioxxterms:ext_relation` property. 

`rioxxterms:ext_relation` is further refined by a series of attributes, which **SHOULD** be included (where applicable):

* `rel`
* `coar_type`
* `coar_version`

`rioxxterms:ext_relation` **MUST** include the `coar_type` attribute. The `coar_version` attribute  **MAY** be included (where appropriate), if the related resource is a publication.

### Attributes
1. *rel*: <mark>needs definition</mark>
1. *coar_type*:  When used, the `coar_type` attribute **MUST** contain a value which is an identifier from the [COAR Resource Types Vocabulary](http://purl.org/coar/resource_type/). For example, for the common case of the related resource being a PDF of a journal article, the **RECOMMENDED** value would be `http://purl.org/coar/resource_type/c_6501`. The [COAR Resource Types Vocabulary](http://purl.org/coar/resource_type/) accommodates a diverse range of resource types. `dc:relation` can therefore also be used to communicate the existence of harvestable related data or software, such as by types [experimental data](http://purl.org/coar/resource_type/63NG-B465) or [research software](http://purl.org/coar/resource_type/c_c950).
2. *coar_version*: When used, the `coar_version` attribute **MUST** contain a value which is an identifier from the [COAR Version Types Vocabulary](http://purl.org/coar/version/).



## Examples:

**Example 1:**
<mark>describe this example</mark>

```xml
<rioxxterms:ext_relation
        rel="cite-as"
        coar_type="https://purl.org/coar/resource_type/c_6501"
        coar_version="https://purl.org/coar/version/c_970fb48d4fbd8a85">
    https://doi.org/10.1007/s11229-020-02724-x
</rioxxterms:ext_relation>
```

**Example 2**

<mark>describe this example</mark>

```xml
<rioxxterms:ext_relation
        rel="cite-as"
        coar_type="https://purl.org/coar/resource_type/c_ddb1">
    https://doi.org/10.15129/5d28213e-8f9f-402a-b550-fc588518cb8b
</rioxxterms:ext_relation>
```

**Example 3**

<mark>describe this example</mark>

```xml
<rioxxterms:ext_relation
        rel="cite-as"
        coar_type="https://purl.org/coar/resource_type/QH80-2R4E">
    https://doi.org/10.5281/zenodo.3478185
</rioxxterms:ext_relation>
```