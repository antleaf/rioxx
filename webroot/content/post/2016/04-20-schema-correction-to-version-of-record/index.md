---
creators: ["Paul Walk"]
categories: []
date: 2016-04-20T09:31:27+01:00
description: ""
draft: false
tags: []
title: "Schema correction: rioxxterms:version_of_record"
topics: []
aliases:
- "/2016/04/20/Schema-correction-rioxxtermsversion_of_record/"
---
Pierre Lasou from Bibliothèque de l'Université Laval reported a 'bug' in RIOXX 2.0. While the documentation consistently refers to a property called 'rioxxterms:version_of_record', the schema XSD incorrectly includes a property called 'rioxxterms:version-of-record'.

I have updated the schema XSD to use the correct form - rioxxterms:version_of_record. This for two reasons:

1. underscores, rather than hyphens, are used consistently elsewhere in the RIOXX profile
2. the only examples of this property I can find 'in the wild' have used this version

So, for the avoidance of any doubt, the correct version to use is:

````
rioxxterms:version_of_record
````