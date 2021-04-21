---
date: '2020-10-08T10:00:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:resource_exposed_date
cardinality: Zero or one
requirement: Optional
metadata_profile: v3-0-draft
---
This element captures the date on which ***the resource*** is made publicly available. Element content **MUST** be encoded according to the [W3CDTF](https://www.w3.org/TR/NOTE-datetime) (a profile of [ISO 8601](https://www.iso.org/standard/40874.html)) which typically follows the following format: YYYY-MM-DD.

Examples:
<pre><code class="language-xml">&lt;rioxxterms:resource_exposed_date&gt;
    2019-02-23
&lt;/rioxxterms:resource_exposed_date&gt;
</code></pre>

or

<pre><code class="language-xml">&lt;rioxxterms:resource_exposed_date&gt;
    2020-07-16T19:20+01:00
&lt;/rioxxterms:resource_exposed_date&gt;
</code></pre>


Repositories will typically fulfil `rioxxterms:resource_exposed_date` if ***the resource*** is made publicly visible immediately upon deposit, or when ***the resource*** embargo ends. 

This element should not be confused `rioxxterms:record_public_release_date`. 

