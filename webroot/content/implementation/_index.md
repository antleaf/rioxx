---
categories: []
date: 2015-10-30T15:06:21Z
description: ""
draft: false
tags: []
title: Implementation
topics: []
---

The RIOXX Metadata Application Profile has been implemented in a number of systems. This page provides links to:

* [re-usable software components](#software_components)
* [systems which *consume* RIOXX metadata](#consuming_systems)

<a name="software_components"></a>
## Software components

#### EPrints repository plugin
This plugin is [funded and supported by Jisc](https://www.jisc.ac.uk/repository-technical-support). It adds the following functionality to an EPrints repository:

* capture of additional metadata required by the RIOXX application profile
* measurement of RIOXX compliance across the repository
* exposure of RIOXX-compliant XML records (via OAI-PMH) for sharing with funders and governing bodies

The plugin can be installed from the [EPrints Bazaar](http://bazaar.eprints.org/). The source-code is available on [GitHub](https://github.com/eprintsug/rioxx2).

#### DSpace (versions 3,4 or 5) repository patches
These patches are [funded and supported by Jisc](https://www.jisc.ac.uk/repository-technical-support). They add the following functionality to a DSpace respository:

* RIOXX-related fields in the submission forms
* a way to expose only RIOXX-compliant items
* live lookup into the Fundref registry for funder identifiers

The patches are available on request by email to [info@atmire.com](mailto:info@atmire.com).

------

<a name="consuming_systems"></a>
## Systems consuming RIOXX metadata
#### One Repo
The One Repo is a platform which "aims to make the entire open-access scholarly record available via a Web UI, embeddable widgets and various web-services, as well providing all of the metadata for direct download".

* [One Repo live demo](http://onerepo.net)
* [One Repo blog](http://blog.onerepo.net/)
* [One Repo white paper](http://onerepo.net/onerepo-whitepaper.pdf)

#### CORE
CORE is a harvesting and aggregation system which offers "seamless access to millions of open access research papers" and provides value-added services from this aggregation.

* [CORE online service](https://core.ac.uk)
* [CORE blog](https://blog.core.ac.uk)


