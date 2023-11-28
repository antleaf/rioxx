---
date: '2023-11-28T10:21:43+00:00'
draft: false
type: metadata_profile_property
title: dc:identifier
cardinality: Exactly one
requirement: Mandatory
metadata_profile: v3-0-final
---
`dc:identifier` **MUST** contain an identifying HTTP(S) URI of the repository 'landing page' describing this resource. The landing page should provide links to related resources. We **RECOMMEND** using FAIR Signposting ([signposting.org/FAIR](http://signposting.org/FAIR)) to assist machine agents in navigating from the landing page to the relevant resources. The value of `dc:identifier` does not have to be a persistent identifier (PID), instead, in order to facilitate indexing by machine agents, it is **RECOMMENDED** that `dc:identifier` contains a direct HTTP(S) URI of the landing page, i.e. resolving `dc:identifier` **SHOULD** be possible without the use of HTTP redirection.

### Example
A typical example of this property is provided below, where the direct HTTP(S) URI of the repository landing page is expressed.

```xml
<dc:identifier>https://www.repository.cam.ac.uk/items/c6173013-1e2f-4818-9d1e-98a0f189c7c8</dc:identifier>
```

`dc:identifier` can be supplemented by using `dc:relation` to declare the local repository PID for the corresponding resource, in this case a DOI.

```xml
<dc:relation rel="cite-as">https://doi.org/10.17863/CAM.101562</dc:relation>
```

