---
date: '2020-11-18T11:00:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:version_of_record
cardinality: Zero or one
requirement: Recommended
metadata_profile: v3-0-rc-2
---

<mark>Is this necessary at 'root' level, when `version_of_record` is likely to be encoded with greater specificity at file level, within `rioxxterms:item` and/or `rioxxterms:relation`? @g3om4c</mark>

<mark>I think we should definitely remove this, for the reason George suggests above (Paul)</mark>

<s>
This property **MUST** contain an HTTP(S) URI which is a persistent identifier for the published 'version of record' of *the resource*. If a DOI has been issued by the publisher then this **MUST** be used (and such a DOI **MUST** be represented in its HTTP(S) form). For example:

```xml
<rioxxterms:version_of_record>
    https://doi.org/10.1103/PhysRevD.102.043015
</rioxxterms:version_of_record>
```
</s>
