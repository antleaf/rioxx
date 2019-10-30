---
creators: ["Paul Walk"]
categories: []
date: 2016-03-29T17:18:13+01:00
description: ""
draft: false
tags: []
title: RIOXX and metadata only records
topics: []
aliases:
- "/2016/03/29/RIOXX-and-metadata-only-records/"
---

I received the following query from Emma Sansby, Head of Library Services at Bishop Grosseteste University:

> I am currently leading a project to implement Eprints (hosted and supported by ULCC) at my institution.  We have the RIOXX plugin installed and I have a question about the licence_ref attribute.
> 
> I am creating a metadata-only journal article record into our repository which includes a DOI link to the publisher’s website.  When I get to the RIOXX page I am forced to enter something under licence_ref as the attribute is mandatory, even though it’s a metadata-only record.  What I’m not sure about is whether, with a metadata-only record, the licence information I enter needs to relate to the terms of use for the metadata itself, or to the terms of use for article out on the publisher’s website.
> 
> Can you provide any guidance?

A good question, and an interesting one!

My initial response to this would be to say that RIOXX is designed to allow reporting on the status of open access papers, and that without such a paper to describe, the RIOXX record is effectively meaningless. If the published version of a paper (the 'version of record') is itself open access, then the RIOXX record could describe that (the rioxxterms:version_of_record and the dc:identifier properties would contain the same value - a URL pointing to the open access paper.)

Is this sufficient answer to Emma's question? I'd be interested to hear what others think - especially if you have encountered this issue. Please feel free to leave a comment below - even if it is simply to say that this is also a concern for you.
