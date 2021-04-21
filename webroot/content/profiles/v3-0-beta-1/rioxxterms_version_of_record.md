---
date: '2020-11-18T11:00:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:version_of_record
cardinality: Zero or one
requirement: Recommended
metadata_profile: v3-0-draft
---
This field **MUST** contain an HTTP(S) URI which is a persistent identifier for the published version of ***the resource***. If a DOI has been issued by the publisher then this *MUST* be used. Such a DOI **MUST** be represented in its HTTPS form, for example:

<pre><code class="language-xml">&lt;rioxxterms:version_of_record&gt;
    https://doi.org/10.1103/PhysRevD.102.043015
&lt;/rioxxterms:version_of_record&gt;
</code></pre>

