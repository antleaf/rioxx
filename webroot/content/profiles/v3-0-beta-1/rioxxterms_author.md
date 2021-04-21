---
date: '2020-10-28T14:26:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:author
cardinality: One or more
requirement: Mandatory
metadata_profile: v3-0-draft
---
The author of ***the resource*** may be a person, organisation or service, but is most commonly a person. This element **SHOULD** take an optional attribute called *id*, which **MUST** contain an HTTP(S) URI which uniquely identifies the author. Where there is more than one author, a separate *rioxxterms:author* element **MUST** be used for each. As many authors may be entered as required. 

The ideal use of this element is to include both an HTTP(S) URI in the *id* attribute, and a text string in the body of the element, thus:
<pre><code class="language-xml">&lt;rioxxterms:author id="https-uri-for-this-author-entity"&gt;
    name-of-this-author-entity
&lt;/rioxxterms:author&gt;
</code></pre>

Where the author is a person, the **RECOMMENDED** format is to add text in the form Last Name, First Name(s), and to include an [ORCID](http://orcid.org) ID, if known, in its HTTPS URI form, e.g. 

<pre><code class="language-xml">&lt;rioxxterms:author id="https://orcid.org/0000-0001-5305-9450"&gt;
    Riccardi, Annalisa
&lt;/rioxxterms:author&gt;
</code></pre>


Where the author is an organisation, the **RECOMMENDED** format is to add the official name of the organisation, and to include an [ISNI](http://isni.org) ID, if known, in its HTTP(S) URI form, e.g.

<pre><code class="language-xml">&lt;rioxxterms:author id="https://isni.org/isni/0000000419368139"&gt;
    University of Strathclyde
&lt;/rioxxterms:author&gt;
</code></pre>


Where the *rioxxterms:author* element appears multiple times for one record, it **CAN** be assumed that the order is significant, in that the first element describes the &#39;first named author&#39; of ***the resource***. In order to make this more explicit, an extra attribute, *first-named-author*, **SHOULD** be used to indicate which of the *rioxxterms:author* elements describes the first named author of ***the resource***, thus:

<pre><code class="language-xml">&lt;rioxxterms:author id="https://orcid.org/0000-0001-5305-9450" first-named-author="true"&gt;
    Riccardi, Annalisa
&lt;/rioxxterms:author&gt;
</code></pre>

