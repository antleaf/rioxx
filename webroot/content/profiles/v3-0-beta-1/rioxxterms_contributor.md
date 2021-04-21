---
date: '2020-10-28T14:58:43+00:00'
draft: false
type: metadata_profile_property
title: rioxxterms:contributor
cardinality: Zero or more
requirement: Optional
metadata_profile: v3-0-draft
---
This field is designed to describe an entity – for example the name of a person, organisation or service – responsible for making contributions to the content of ***the resource***. As many rioxxterms:contributor elements may be entered as required. This element **SHOULD** take an optional attribute called *id*, which **MUST** contain an HTTP(S) URI which uniquely identifies the contributor. The ideal use of this element is to include both an HTTP(S) URI in the *id* attribute, and a text string in the body of the element, thus:

<pre><code class="language-xml">&lt;rioxxterms:contributor id="https-uri-for-this-contributor-entity"&gt;
    name-of-this-contributor-entity
&lt;/rioxxterms:contributor&gt;
</code></pre>


Where the contributor is a person, the **RECOMMENDED** format is to add text in the form Last Name, First Name(s), and to include an [ORCID](http://orcid.org) ID, if known, in its HTTPS URI form, e.g.

<pre><code class="language-xml">&lt;rioxxterms:contributor id="https://orcid.org/0000-0002-1919-4138"&gt;
    Milgrom, Paul
&lt;/rioxxterms:contributor&gt;
</code></pre>

Where the contributor is an organisation, the **RECOMMENDED** format is to add the official name of the organisation, and to include an [ISNI](http://isni.org) ID, if known, in its HTTPS URI form, e.g.

<pre><code class="language-xml">&lt;rioxxterms:contributor id="https://isni.org/isni/0000000419368956"&gt;
    Stanford University
&lt;/rioxxterms:contributor&gt;
</code></pre>

