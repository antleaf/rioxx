---
title: RIOXX - Release candidate application profile and guidelines
date: 2013-03-18T00:00:00+00:00
description: 
draft: false
tags: []
topics: []
categories: []
creators: ["Paul Walk"]
aliases:
- "/2013/03/18/RIOXX-Release-candidate-application-profile-and-guidelines/"
---

We are pleased to announce that version 0.9 of the RIOXX guidelines and application profile are available for public comment:


* [UK Metadata Guidelines for Open Access Repositories](http://docs.rioxx.net/guidelines/UK_Metadata_Guidelines_v_0.9.pdf)
* [RIOXX application profile](http://www.rioxx.net/v0-9/)

These releases should be considered as 'release candidates'. Work is under way to commission plugins/patches for both ePrints and DSpace to help institutional repositories to implement the guidelines and application profile. The technical specifications for this work will also be made freely available for developers to implement support for other platforms.

<!-- ----

#### Comments

##### Comment by Anna Clements on 2013/03/25 at 11:50

Quick question on the list of funders … is this a service that will be maintained as an authority list and we can therefore use for quality control in our CRIS or IR?
Where is the list from and who will maintain it going forward?

----

##### Comment by James Toon on 2013/03/27 at 10:36

On the funder ID requirement rioxxterms.project.id I have a little concern over the need to have the exact award reference because we have many cases here where the ID held on our system may have a different suffix i.e. ST/K001234/1 might actually be ST/K001234/2 in our system because the PI might have transferred in from another institution etc... hence we wouldn’t be able to comply.

I was also going to ask much the same thing as Anna – also about whether the funding list will be maintained and/or could be extended to include former names (previously known as, merged with etc) plus some date info to add to the former categories.

BTW – I also note that the url in the document is http://docs.rioxx.net.funders and should be http://docs.rioxx.net/funders

----

##### Comment by [Petr Knoth](http://people.kmi.open.ac.uk/petr/) on 2013/03/28 at 22:47

Hi Paul,

I had a look on the 0.9 draft of the RIOXX specification and have two questions/suggestions.

1) dc:rights. I find it interesting that you decided not to follow the OpenAire guidelines (their vocabulary), but in my view your recommendation looks more descriptive (and logical). Perhaps this non-compliance with OpenAire could be solved by mapping your (CreativeCommons) vocabulary to the OpenAire vocabulary (which I imagine can be done easily).

2) dc:identifier

The RIOXX guidelines say about the dc:identifier field the following:

> dc:identifier

> cardinality: Exactly one

> This field MUST contain a globally unique and persistent identifier for the resource being described. The identifier SHOULD be an HTTP URI that can be de-referenced (and is, thus, actionable). The purpose of this field is to allow access to the resource, therefore it is RECOMMENDED that this identifier should point to the actual resource being described by the RIOXX record (typically a PDF file), rather than to an intermediary resource such as a repository web page. This resource SHOULD be a version of the resource held in the local repository.

I really like that RIOXX goes quite far in this, but think it can go even a bit further. A few month ago, I drafted a paper - [From Open Access Metadata to Open Access Content](http://core-project.kmi.open.ac.uk/files/oa-metadata-to-oa-content.pdf) in which I was looking at how repositories reference full-texts. I came up with two principles/recommendations that would, I believe, really help content aggregators. I think they are already quite consistent with the approach you are proposing. 

The first principle, which you find on page 3 of the paper, says:

> Open repositories should always establish a link from the metadata record to the item the metadata record describes using a de-referencable identifier pointing to the version held in the repository. The de-referencable identifier should be provided in the appropriate metadata element in the used metadata format (i.e. dc:identifier in the case of Dublin Core).

> The implications of the principle. Repositories can use different metadata standards to describe resources offered using OAI-PMH. For example, repositories exposing complex objects might want to describe them in MPEG21-DIDL or METS. However, at minimum they must offer Dublin Core metadata, where each Dublin Core record uses at least one of its dc:identifiers to identify the described object (content in the repository) using a dereferencable identifier, i.e. the identifier must resolve to the object it identifies (not into another identifier). In the special case of Dublin Core, which can be used to describe simple objects only (Van de Sompel, 2004), if more dereferencable URIs are present (which is syntactically correct), we suggest to use the first dereferencable identifier as the identifier of the described object. The identifier should resolve to the version of the object held in the repository, which is important for being able to acquire repository content statistics.

The second principle (page 4) says:

> Open repositories must provide universal access to machines with the same level of access as humans have. It is the role of open repositories to allow machines harvest the entire  content of the repository in a reasonable time to enable harvesting systems to acquire and maintain up-to-date information about the repository content.

> The implications of the principle. Repositories should ensure their content could be access by programs, for example to collect data for text-mining or indexing. This access must be universal, i.e. it should not discriminate or provide an unfair advantage to any particular system (with the exception of abusive behavior). Programs, such as content harvesters, must be allowed to access the repository at such frequency that allows them to keep information about the repository current. However, some repositories might contain both OA materials as well as non-OA materials. In such cases, it is acceptable and, in fact, beneficial to clearly restrict access to the non-OA materials. If a repository does not comply with this principle, it should not be considered an Open Repository.

I know you are in RIOXX quite logically restricting yourself to DC only. Since repositories often use multiple dc:identifier fields to describe a single resource using a DC record, I suggest at least one (and possibly the first one) of the dc:identifiers to be a global de-referenceble identifier of a resource stored in that repository, i.e. the identifier resolves to a URL under the domain of that repository. It is absolutely OK to specify other global identifiers in the next dc:identifier fields. These can resolve to items outside of that repository. 

I personally do not think that there should be necessarily just one dc:identifier and most repositories do, in fact, use many instances of dc:identifier to describe a single record. For example, a repository can specify a dc:identifier for its local copy and then reference the copy at the publisher's website. 

I really like that you require the item to be in the local repository, because this will, for example, allow to calculate repository statistics in terms of their content. This is crucial in order to be able to monitor full-text repository deposits (green OA) and compare them with gold OA (this is also why we need higher cardinality for dc:identifiers - to allow people link to both copies in the repository and outside of the repository). It is also essential in order to be able to verify compliance with the new OA policies (e.g. RCUK) regarding embargoes. For instance, it should be possible to check that an item is made available by the repository when the embargo expires. In addition, it would likely also help mitigate the second issue of machine access to resources described in the above mentioned paper. So overall, I think this should not be just SHOULD but in case the metadata record describes an item that is available it should be MUST. 

I would suggest the following phrasing for dc:identifier:

> dc:identifier

> Cardinality: One or more

> This field MUST contain a globally unique and persistent identifier for the resource being described. If the actual described resource is available, the identifier MUST be an HTTP URI that can be de-referenced (and is, thus, actionable) and resolves to the described resource held in the local repository. The purpose of this field is to allow access to the resource, therefore it is REQUIRED that this identifier should point to the actual resource being described by the RIOXX record (typically a PDF file), rather than to an intermediary resource such as a repository web page. The following dc:identifiers SHOULD also be de-referencable, but can link to content not held in the local repository, for example to the publisher's website.

Does it make sense? 

Sorry this is so long ...

Regards,

Petr

----

##### Comment by [Petr Knoth](http://people.kmi.open.ac.uk/petr/) on 2013/03/28 at 23:14

Forgot one more point about access to machines. Would suggest the following phrasing for dc:identifier:

dc:identifier
Cardinality: One or more

This field MUST contain a globally unique and persistent identifier for the resource being described. If the actual described resource is available, the identifier MUST be an HTTP URI that can be de-referenced (and is, thus, actionable) and resolves to the described resource held in the local repository. The purpose of this field is to allow access to the resource, therefore it is REQUIRED that this identifier should point to the actual resource being described by the RIOXX record (typically a PDF file), rather than to an intermediary resource such as a repository web page. Machine access to this resource MUST NOT be prevented (for example by specifying the disallow directive or excessive crawl-delay in the repository robots.txt file). The following dc:identifiers SHOULD also be de-referencable, but can link to content not held in the local repository, for example to the publisher’s website. -->