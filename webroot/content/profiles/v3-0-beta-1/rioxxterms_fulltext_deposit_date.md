---
date: '2020-10-08T10:00:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:fulltext_deposit_date
cardinality: Zero or one
requirement: Optional
metadata_profile: v3-0-draft
---

This element takes the date on which ***the resource*** was first deposited, irrespective of any relevant embargoes or dark archiving, and irrespective of any subsequent file replacement(s). Element content **MUST** be encoded according to the [W3CDTF](https://www.w3.org/TR/NOTE-datetime) (a profile of [ISO 8601](https://www.iso.org/standard/40874.html)) which typically follows the following format: YYYY-MM-DD.

Examples:
<pre><code class="language-xml">&lt;rioxxterms:fulltext_deposit_date&gt;
    2019-02-23
&lt;/rioxxterms:fulltext_deposit_date&gt;

&lt;rioxxterms:fulltext_deposit_date&gt;
    2020-07-16T19:20+01:00
&lt;/rioxxterms:fulltext_deposit_date&gt;
</code></pre>

It is anticipated that in some circumstances `rioxxterms:fulltext_deposit_date` will be captured and exposed in repository metadata when the resource described is under temporary embargo or temporary dark archiving. 

