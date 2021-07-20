---
creators: ["George Macgregor"]
categories: []
date: 2021-07-06
description: ""
draft: false
tags: []
title: "RIOXX metadata application profile v 3.0 beta draft released"
topics: []
aliases:
---

Those of you following the status of RIOXX will be aware that [a new governance group was formed](https://www.rioxx.net/post/2019/10-31-new-governance-group-and-plans-for-revision/) in late 2019 under the auspices of [UKCORR](https://www.ukcorr.org/) (RIOXX Governance Group - RGG). Following [a period of consultation and review](https://www.ukcorr.org/2020/08/25/rioxx-as-an-effective-mechanism-for-the-efficient-exposure-and-aggregation-of-repository-content/), the RGG is pleased to announce the publication of a [beta draft of **RIOXX v 3.0** for public comment](/profiles/v3-0-beta-1/).

v 3.0 delivers minor updates to refresh the profile but also includes some major changes, such as the removal of `<ali:free_to_read>`  -- removed owing to inconsistent application across the sector and its creation of internal  inconsistency in RIOXX; and the addition of a new property: `<rioxxterms:record_public_release_date>` to better model the deposit-exposure lifecycle of deposited digital resources. A significant alteration to the application of `<dc:identifier>` has also been introduced. We hope to better explain the rationale for specific changes in a forthcoming working paper or journal article, as well as re-articulate the benefits of RIOXX adoption for the purposes of discovery and aggregation. This will arrive in the near future.

In the meantime, we again solicit feedback from the community about the beta draft. Comments or issues can be raised through the [RIOXX GitHub repository](https://github.com/antleaf/rioxx/issues) or by contacting the [RGG Chair](https://geo-mac.github.io/).

Readers are encouraged to review v 3.0 in its entirety; substantive changes can nevertheless be summarised as follows:

- `<ali:license_ref>`, `<rioxxterms:author>`, `<rioxxterms:contributor>`, `<rioxxterms:project>`, `<rioxxterms:version_of_record>` **updated** to explicitly note HTTPS use where URI values are specified.
- **Removed** the `<ali:free_to_read>` property.
- **Removed** the `<rioxxterms:apc>` property.
- Addition of the **new** property: `<rioxxterms:record_public_release_date>`, encoded according to ISO8601/W3CDTF.
- `<rioxxterms:publication_date>` **updated** to specify encoding as per ISO8601/W3CDTF, including resources with seasonal publication dates.
- Controlled list of types in  `<rioxxterms:type>` **removed** and **updated** to specify the [COAR Controlled Vocabulary Resource Type Genres](http://vocabularies.coar-repositories.org/documentation/resource_types/).
- Replacement of XML 'id' attributes within properties with new 'uri' attribute.
- Modification to the application of `<dc:identifier>` and `<dc:relation>`.

Perhaps the most significant change in v 3.0 is the latter update relating to  `<dc:identifier>` and `<dc:relation>`. It is a significant change because it departs from the convention established in prior versions of the profile whereby `<dc:identifier>` captured an identifier pointing to the actual resource being described by the RIOXX record (typically a file), rather than an intermediary resource such as a repository abstract page. RIOXX v 3.0 does not prohibit the continued use of `<dc:identifier>`in this way but instead recommends a change in its application and introduces new attributes to be used with `<dc:relation>` to accommodate multiple 'expressions' of the same 'work'. This is supplemented by the 'uri', 'deposit_date' and 'resource_exposed_date' attributes, and the 'type' attribute, the latter defined as per [schema.org](https://schema.org/). This changes helps to communicate the HTTP(S) location of expressions.

More generally, RIOXX v 3.0 moves away from using the XML 'id' attribute across the profile to communicate URI(s) in instances where it is necessary to uniquely identify property content. This has resulted in the introduction of the 'uri' attribute as an alternative to 'id' which, in v 3.0, specifically affects `<rioxxterms:author>`, `<rioxxterms:contributor>`, `<rioxxterms:publisher>` and `<rioxxterms:type>`. The [id attribute has strict usage under the W3C XML specification](https://www.w3.org/TR/xml/#sec-attribute-types) and it was acknowledged to be undesirable to expand its usage within v 3.0.

Striking a balance between the desire to data model perfectly and the need to keep the profile easily adoptable has been a difficult task for the RGG. A principal motivation for RIOXX and the work of the RGG was to facilitate the improved harvesting, aggregation and discovery of repository content -- and this is what we have tried to remain focused on. What is presented in v 3.0 may therefore be imperfect in certain respects but, within our parameters, nevertheless constitutes a useful update to the profile.

We welcome feedback!
