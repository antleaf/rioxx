---
date: '2023-10-19T10:21:43+00:00'
draft: false
type: metadata_profile_property
title: dc:identifier
cardinality: Exactly one
requirement: Mandatory
metadata_profile: v3-0-final
---
`dc:identifier` **MUST** contain an HTTP(S) URI which is an identifier for the resource. This URI should resolve to, or contain an identifier that can be resolved to, a repository 'landing page' describing this resource. The landing page should provide links to related resources. We recommend using FAIR Signposting ([signposting.org/FAIR](http://signposting.org/FAIR)) to assist machine agents in navigating from the landing page to the relevant resources. 

<!-- @g3om4c - Starting modifying this and then paused. Our intention is that the value of dc:identifier should explicitly *not* be a PID and instead a repository URL to the landing page. However, I paused because some repositories will also present these as URIs too. We should therefore accommodate both, providing neiter is a PID...? -->