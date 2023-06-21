---
date: '2023-06-01T16:04:43+00:00'
draft: false
type: metadata_profile_property
title: "rioxxterms:relation"
cardinality: Zero or more
requirement: Should
metadata_profile: v3-0-rc-2
---

<mark>I have tried to re-write this to be simpler, not sure how successful I have been... (Paul)</mark>

`rioxxterms:relation` is used to convey associations to related scholarly entities. This will typically include alternative 'expressions' of *the resource* (e.g. preprint, VoR, etc.) and/or entities relevant to understanding *the resource*, such as related research data, software, instruments, and so forth. Where such types have been encoded it will be considered to be for the purposes of contributing to the scholarly data graph rather than for assisting harvesting software in locating file content, such as full-text, which is instead enabled via `rioxxterms:item` property.

Each relation **MUST** appear as a separate instance of the `rioxxterms:relation` property. 

`rioxxterms:relation` **MUST** include the `coar_type` attribute. The `coar_version` attribute  **MAY** be included (where appropriate), if the related resource is a publication.

1. *coar_type*:  The `coar_type` attribute **MUST** contain an identifier from the [COAR Resource Types Vocabulary](http://purl.org/coar/resource_type/). For example, for the common case of the related resource being a PDF of a journal article, the **RECOMMENDED** value would be `http://purl.org/coar/resource_type/c_6501`. The [COAR Resource Types Vocabulary](http://purl.org/coar/resource_type/) accommodates a diverse range of resource types.  

2. *coar_version*: The `coar_version` attribute **SHOULD** be included if `rioxxterms:relation` is being used to indicate an associative relation with an alternative 'expression' of the *the resource*, where *the resource* is a publication. Where this is true `coar_version` **MUST** contain an identifier value from the [COAR Version Types Vocabulary](http://purl.org/coar/version/).

<s>
3. *access_rights*: The `access_rights` attribute **SHOULD** be included if authority of assertion exists. Where this is true `access_rights`should take a URI value from the [COAR Access Rights Vocabulary](https://vocabularies.coar-repositories.org/access_rights/), which defines four access states: [embargoed access](http://purl.org/coar/access_right/c_f1cf), [metadata only access](http://purl.org/coar/access_right/c_14cb), [open access](http://purl.org/coar/access_right/c_abf2), [restricted access](http://purl.org/coar/access_right/c_16ec). 
</s>

## Examples:

### Related published article
```xml
<rioxxterms:relation coar_type="https://purl.org/coar/resource_type/c_6501" 
    coar_version="https://purl.org/coar/version/c_970fb48d4fbd8a85">
            https://doi.org/10.1007/s11229-020-02724-x
</rioxxterms:relation>
```

### Related  dataset

```xml
<rioxxterms:relation coar_type="https://purl.org/coar/resource_type/c_ddb1">
            https://doi.org/10.15129/589f7af3-26b3-4a93-b042-fbc8100fc977
</rioxxterms:relation>
```