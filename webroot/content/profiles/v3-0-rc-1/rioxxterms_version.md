---
date: '2022-05-11T10:00:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:version
cardinality: Exactly one
requirement: Mandatory
metadata_profile: v3-0-rc-1
---
This property indicates which 'version' of ***the resource*** is being described. The value of this property **MUST** be one of the following:

* AO
* SMUR
* AM
* P
* VoR
* CVoR
* EVoR
* NA

These terms are adopted from the [NISO RP-8-2008 Journal Article Versions (JAV) standard](https://www.niso.org/publications/niso-rp-8-2008-jav) and have the following meanings:

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