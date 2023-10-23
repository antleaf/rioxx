---
date: '2023-10-19T16:04:43+00:00'
draft: false
type: metadata_profile_property
title: "rioxxterms:ext_relation"
cardinality: Zero or more
requirement: Should
metadata_profile: v3-0-final
---

`rioxxterms:ext_relation` is used to convey external associations to related scholarly entities (i.e. external relations). Such relational associations will be scholarly entities hosted externally or outsider the direct custodianship of the repository asserting the relational associations. Examples of these associations might typically include alternative 'expressions' of *the resource* (e.g. preprint, VoR, etc.) and/or entities relevant to understanding *the resource*, such as related research data, software, code, instruments, and so forth. Where such types have been encoded it will be considered to be for the purposes of contributing to the scholarly data graph and/or end users, rather than for assisting harvesting software in locating file content, such as full-text, which is instead conveyed via `dc:relation` property.

Each external relation **MUST** appear as a separate instance of the `rioxxterms:ext_relation` property. 

`rioxxterms:ext_relation` **MUST** include the `rel` and `coar_type` attributes. The `coar_version` attribute **MAY** be included (where appropriate), if the related resource is a publication.

1. *rel*: The `rel` attribute uses 'typed links' from the [IANA Link Relation Registry](https://www.iana.org/assignments/link-relations/link-relations.xhtml). As Rioxx uses `rioxxterms:ext_relation` to communicate external associations, this attribute will normally be set to "cite-as", e.g. `rel='cite-as'`.

2. *coar_type*:  The `coar_type` attribute **MUST** contain an identifier from the [COAR Resource Types Vocabulary](http://purl.org/coar/resource_type/). For example, for the common case of the related resource being a PDF of a journal article, the **RECOMMENDED** value would be `http://purl.org/coar/resource_type/c_6501`. The [COAR Resource Types Vocabulary](http://purl.org/coar/resource_type/) accommodates a diverse range of resource types.  

3. *coar_version*: The `coar_version` attribute **SHOULD** be included if `rioxxterms:ext_relation` is being used to indicate an associative relation with an alternative 'expression' of the *the resource*, where *the resource* is a publication. Where this is true `coar_version` **MUST** contain an identifier value from the [COAR Version Types Vocabulary](http://purl.org/coar/version/).

## Examples:

### Related published article
```xml
<rioxxterms:ext_relation 
    rel="cite-as"
    coar_type="https://purl.org/coar/resource_type/c_6501" 
    coar_version="https://purl.org/coar/version/c_970fb48d4fbd8a85">
            https://doi.org/10.1007/s11229-020-02724-x
</rioxxterms:ext_relation>
```

### Related  dataset

```xml
<rioxxterms:ext_relation 
    rel="cite-as"            
    coar_type="https://purl.org/coar/resource_type/c_ddb1">
            https://doi.org/10.15129/589f7af3-26b3-4a93-b042-fbc8100fc977
</rioxxterms:ext_relation>
```