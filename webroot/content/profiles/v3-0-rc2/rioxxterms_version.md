---
date: '2022-11-22T10:00:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:version
cardinality: Exactly one
requirement: Mandatory
metadata_profile: v3-0-rc-2


---

This property indicates which 'version' of ***the resource*** is being described. The value of this property uses concepts defined by [NISO RP-8-2008 Journal Article Versions (JAV) standard](https://www.niso.org/publications/niso-rp-8-2008-jav) and adapted by the [COAR Version Types vocabulary]([Controlled Vocabularies for Repositories: Version Types](https://vocabularies.coar-repositories.org/version_types/)). 

The value of the property **MUST** be one of the following:

- [AM](https://vocabularies.coar-repositories.org/version_types/c_ab4af688f83e57aa/)

- [AO](https://vocabularies.coar-repositories.org/version_types/c_b1a7d7d4d402bcce/) 

- [CVoR](https://vocabularies.coar-repositories.org/version_types/c_e19f295774971610/)

- [EVoR](https://vocabularies.coar-repositories.org/version_types/c_dc82b40f9837b551/)

- [NA](https://vocabularies.coar-repositories.org/version_types/c_be7fb7dd8ff6fe43/)

- [P](https://vocabularies.coar-repositories.org/version_types/c_fa2ee174bc00049f/)

- [SMUR](https://vocabularies.coar-repositories.org/version_types/c_71e4c1898caa6e32/)

- [VoR](https://vocabularies.coar-repositories.org/version_types/c_970fb48d4fbd8a85/) 

The value should be supplemented by the corresponding COAR Version Types URI, as per this example for AM ('Accepted Manuscript'):

```xml
<rioxxterms:version uri="https://vocabularies.coar-repositories.org/version_types/c_ab4af688f83e57aa/">
    AM
</rioxxterms:version>
```

These abbreviations are defined by the JAV standard and have the following meanings:

* AO = Author&#39;s Original
* SMUR = Submitted Manuscript Under Review
* AM = Accepted Manuscript
* P = Proof
* VoR = Version of Record
* CVoR = Corrected Version of Record
* EVoR = Enhanced Version of Record
* NA = Not Applicable (or Unknown) 

<!--
Note that `rioxxterms:version` pertains to the version being described. `dc:relation` should be used to encode the location of related file content and their version(s), where applicable. 
-->