---
title: "Crosswalk from RIOXX 2.0 to OpenAIRE 3.0"
date: 2018-01-18T14:58:40+02:00
draft: false
aliases:
- "/crosswalk_rioxx_2_0_openaire_3_0/"
---

This crosswalk has been developed by the RIOXX team at EDINA in close collaboration with technical personnel at OpenAIRE. We would like to thank, in particular, Jochen Schirrwagen and Paolo Manghi for their assistance with this.

For guidance on the exact representation of properties within the OpenAIRE 3.0 metadata profile, please consult the documentation [OpenAIRE Guidelines: For Literature Repositories](https://guidelines.openaire.eu/en/latest/literature/index.html)

The terms **MUST**, **MUST NOT**, **REQUIRED**, **SHALL**, **SHALL NOT**, **SHOULD**, **SHOULD NOT**, **RECOMMENDED**, **MAY**, and **OPTIONAL** used in the table below should be interpreted as described in [RFC 2119](http://www.ietf.org/rfc/rfc2119.txt).

<table class="table table-condensed table-striped sorted-table">
  <thead>
    <tr>
      <th>RIOXX</th>
      <th>OpenAIRE</th>
      <th>Implementation</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <b>ali:free_to_read</b>
        <br/>
        <i>Zero or one</i>
      </td>
      <td>
        <b>dc:rights</b>
        <br/>
        <i>One or more</i>
      </td>
      <td>
        This <strong>MUST</strong> be included, if available.&nbsp;
      </td>
    </tr>
    <tr>
      <td>
        <b>ali:license_ref</b>
        <br/>
        <i>One or more</i>
      </td>
      <td>
        <b>dc:rights</b>
        <br/>
        <i>One or more</i>
      </td>
      <td>
        This <strong>MUST</strong> be included, if available.&nbsp;
      </td>
    </tr>
    <tr>
      <td>
        <b>dc:coverage</b>
        <br/>
        <i>Zero or one</i>
      </td>
      <td>
        <b>dc:coverage</b>
        <br/>
        <i>Zero or more</i>
      </td>
      <td>
        This <strong>SHOULD</strong> be included, if available.&nbsp;
      </td>
    </tr>
    <tr>
      <td>
        <b>dc:description</b>
        <br/>
        <i>Zero or more</i>
      </td>
      <td>
        <b>dc:description</b>
        <br/>
        <i>zero or more</i>
      </td>
      <td>
        This <strong>MUST</strong> be included, if available.&nbsp;
      </td>
    </tr>
    <tr>
      <td>
        <b>dc:format</b>
        <br/><i>Zero or more</i>
      </td>
      <td>
        <b>dc:format</b>
        <br/>
        <i>Zero or more</i>
      </td>
      <td>
        This <strong>SHOULD</strong> be included, if available.&nbsp;If provided in the RIOXX record, values will be in the form of MIME types
      </td>
    </tr>
    <tr>
      <td>
        <b>dc:identifier</b>
        <br/>
        <i>Exactly one</i>
      </td>
      <td>
        <b>dc:identifier</b>
        <br/>
        <i>One or more</i>
      </td>
      <td>
        This <strong>MUST</strong> be included.&nbsp;This value will be in the form of an HTTP URI
      </td>
    </tr>
    <tr>
      <td>
        <b>dc:language</b>
        <br/>
        <i>One or more</i>
      </td>
      <td>
        <b>dc:language</b>
        <br/>
        <i>Zero or more</i>
      </td>
      <td>
        This <strong>MUST</strong> be included.&nbsp;Values will be in the format specified by ISO 639–3
      </td>
    </tr>
    <tr>
      <td>
        <b>dc:publisher</b>
        <br/>
        <i>Zero or more</i>
      </td>
      <td>
        <b>dc:publisher</b>
        <br/>
        <i>Zero or more</i>
      </td>
      <td>
        This <strong>MUST</strong> be included, if available.&nbsp;
      </td>
    </tr>
    <tr>
      <td>
        <b>dc:relation</b>
        <br/>
        <i>Zero or more</i>
      </td>
      <td>
        <b>dc:relation</b>
        <br/>
        <i>Zero or more</i>
      </td>
      <td>
        This <strong>SHOULD</strong> be included, if available.&nbsp;If provided in the RIOXX record, values will be in the form of HTTP URIs
      </td>
    </tr>
    <tr>
      <td>
        <b>dc:source</b>
        <br/>
        <i>Zero or one</i>
      </td>
      <td>
        <b>dc:source</b>
        <br/>
        <i>Zero or more</i>
      </td>
      <td>
        This <strong>SHOULD</strong> be included, if available.&nbsp;If provided in the RIOXX record, the values will normally be in the form of an ISBN13 number (although this is not guaranteed)
      </td>
    </tr>
    <tr>
      <td>
        <b>dc:subject</b>
        <br/>
        <i>Zero or more</i>
      </td>
      <td>
        <b>dc:subject</b>
        <br/>
        <i>Zero or more</i>
      </td>
      <td>
        This <strong>MUST</strong> be included, if available.&nbsp;
      </td>
    </tr>
    <tr>
      <td>
        <b>dc:title</b>
        <br/>
        <i>Exactly one</i>
      </td>
      <td>
        <b>dc:title</b>
        <br/>
        <i>One or more</i>
      </td>
      <td>
        This <strong>MUST</strong> be included.&nbsp;
      </td>
    </tr>
    <tr>
      <td>
        <b>dcterms:dateAccepted</b>
        <br/>
        <i>Exactly one</i>
      </td>
      <td>
        <b>dc:date</b>
        <br/>
        <i>One or more</i>
      </td>
      <td>
        <p>This <strong>MUST</strong> be included.&nbsp;The RIOXX property (in ISO8601 &lsquo;YYYY-MM-DD&rsquo; format) <strong>MUST</strong> be translated into the appropriate OpenAIRE URI (info:eu-repo/semantics/dateAccepted/YYYY-MM-DD).</p>
        <p>Example: RIOXX property:</p>
<pre>
<code>&lt;dcterms:dateAccepted&gt;
  2015-03-16
&lt;/dcterms:dateAccepted&gt;</code>
</pre>
        <p>becomes OpenAIRE property:</p>
<pre>
<code>&lt;dc:date&gt;
  info:eu-repo/semantics/dateAccepted/2015-03-16
&lt;/dc:date&gt;</code>
</pre>
      </td>
    </tr>
    <tr>
      <td>
        <b>rioxxterms:apc</b>
        <br/>
        <i>Zero or one</i>
      </td>
      <td>
        &nbsp;
      </td>
      <td>
        This <strong>MUST NOT</strong> be included.&nbsp;There is no mapping from RIOXX to OpenAIRE for this property, so it <strong>MUST</strong> be ignored
      </td>
    </tr>
    <tr>
      <td>
        <b>rioxxterms:author</b>
        <br/>
        <i>One or more</i>
      </td>
      <td>
        <b>dc:creator</b>
        <br/>
        <i>One or more</i>
      </td>
      <td>
        <p>This <strong>MUST</strong> be included.&nbsp;Where the RIOXX property has the optional ID attribute included, this must be appended to the text content of the OpenAIRE property, parenthesised with square brackets.</p>
        <p>Example: RIOXX property:</p>
<pre>
<code>&lt;rioxxterms:author id=&quot;http://orcid.org/0000-0002-1395-3092&quot;&gt;
  Lawson, Gerald
&lt;/rioxxterms:author&gt;</code>
</pre>
        <p>
          becomes OpenAIRE property:
        </p>
<pre>
<code>&lt;dc:creator&gt;
  Lawson, Gerald [http://orcid.org/0000-0002-1395-3092]
&lt;/dc:creator&gt;</code>
</pre>
      </td>
    </tr>
    <tr>
      <td>
        <b>rioxxterms:contributor</b>
        <br/>
        <i>Zero or more</i>
      </td>
      <td>
        <b>dc:contributor</b>
        <br/>
        <i>Zero or more</i>
      </td>
      <td>
        <p>This <strong>SHOULD</strong> be included, if available.&nbsp;Where the RIOXX property has the optional ID attribute included, this must be appended to the text content of the OpenAIRE property, parenthesised with square brackets.</p>
        <p>Example: RIOXX property:</p>
<pre>
<code>&lt;rioxxterms:contributor id=&quot;http://isni.org/isni/0000000419367988&quot;&gt;
  University of Edinburgh
&lt;/rioxxterms:contributor&gt;</code>
</pre>
        <p>becomes OpenAIRE property:</p>
<pre>
<code>&lt;dc:contributor&gt;
  University of Edinburgh [http://isni.org/isni/0000000419367988]
&lt;/dc:contributor&gt;</code>
</pre>
      </td>
    </tr>
    <tr>
      <td>
        <b>rioxxterms:project</b>
        <br/>
        <i>One or one</i>
      </td>
      <td>
        <b>dc:relation</b>
        <br/>
        <i>Zero or more</i>
      </td>
      <td>
        <p>This <strong>MUST</strong> be included.&nbsp;The RIOXX property includes the ‘project ID’ as provided by the funder. Funding information available and supported by OpenAIRE can be found at <a href="http://api.openaire.eu/">http://api.openaire.eu/</a>. Where the funder is the European Commision, the mapping will be carried out as indicated in the following example:</p>
        <p>RIOXX property:</p>
<pre>
<code>&lt;rioxxterms:project
  funder_name=&quot;European Commission&quot;
  funder_id=&quot;http://isni.org/isni/000000012162673X&quot;
&gt;
  info:eu-repo/grantAgreement/EC/FP7/244909/EU/Making Capabilities Work/WorkAble
&lt;/rioxxterms:project&gt;</code>
</pre>
        <p>becomes OpenAIRE property:</p>
<pre>
<code>&lt;dc:relation&gt;
  info:eu-repo/grantAgreement/EC/FP7/244909/EU/Making Capabilities Work/WorkAble
&lt;/dc:relation&gt;</code>
</pre>
      </td>
    </tr>
    <tr>
      <td>
        <b>rioxxterms:publication_date</b>
        <br/>
        <i>Zero or one</i>
      </td>
      <td>
        <b>dc:date</b>
        <br/>
        <i>One or more</i>
      </td>
      <td>
        <p>This <strong>MUST</strong> be included, if available and in a compatible format.&nbsp;If the RIOXX property is provided in ISO8601 &lsquo;YYYY-MM-DD&rsquo; format then <strong>MUST</strong> be simply mapped into the OpenAIRE dc:date property</p>
        <p>Example: RIOXX property:</p>
<pre>
<code>&lt;rioxxterms:publication_date&gt;
  2015-03-16
&lt;/rioxxterms:publication_date&gt;</code>
</pre>
        <p>becomes OpenAIRE property:</p>
<pre>
<code>&lt;dc:date&gt;
  2015-03-16
&lt;/dc:date&gt;</code>
</pre>
        <p>or, RIOXX property:</p>
<pre>
<code>&lt;rioxxterms:publication_date&gt;
  2015
&lt;/rioxxterms:publication_date&gt;</code>
</pre>
        <p>becomes OpenAIRE property:</p>
<pre>
<code>&lt;dc:date&gt;
  2015
&lt;/dc:date&gt;</code>
</pre>
        <p>However, rioxxterms:publication_date does not constrain the format of its values so entries such as &lsquo;Spring, 2015&rsquo;, while not permissible in OpenAIRE, are perfectly possible in RIOXX. In such cases, the mapping process may choose to parse the permissible value from the RIOXX property to use in the OpenAIRE property - so:</p>
        <p>RIOXX property:</p>
<pre>
<code>&lt;rioxxterms:publication_date&gt;
  Spring, 2015
&lt;/rioxxterms:publication_date&gt;</code>
</pre>
        <p>becomes OpenAIRE property:</p>
<pre>
<code>&lt;dc:date&gt;
  2015
&lt;/dc:date&gt;</code>
</pre>
      </td>
    </tr>
    <tr>
      <td>
        <b>rioxxterms:type</b>
        <br/>
        <i>One or one</i></td>
      <td>
        <b>dc:type</b>
        <br/>
        <i>One or more</i></td>
      <td>
        This <strong>MUST</strong> be included.&nbsp;This must use the controlled vocabulary mapping specified below in the table called <em>Vocabulary mapping: Publication Types</em>
      </td>
    </tr>
    <tr>
      <td>
        <b>rioxxterms:version</b>
        <br/>
        <i>One exactly</i>
      </td>
      <td>
        <b>dc:relation</b>
        <br/>
        <i>One exactly</i>
      </td>
      <td>
        This <strong>MUST</strong> be included.&nbsp;This must use the controlled vocabulary mapping specified below in the table called <em>Vocabulary mapping: Publication Versions</em>
      </td>
    </tr>
    <tr>
      <td>
        <b>rioxxterms:version_of_record</b>
        <br/>
        <i>Zero or one</i>
      </td>
      <td>
        <b>dc:relation</b>
        <br/>
        <i>Zero or more</i>
      </td>
      <td>
        This <strong>MUST</strong> be included, if available.&nbsp;If provided in the RIOXX record, value will be in the form of an HTTP URI
      </td>
    </tr>
  </tbody>
</table>

<br />
<br />

<h2>Vocabulary mapping: Publication Types</h2>
<table class="table table-condensed table-striped sorted-table">
  <thead>
    <tr>
      <th>RIOXX</th>
      <th>OpenAIRE</th>
      <th>Notes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Book</td>
      <td>info:eu-repo/semantics/book</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>Book Chapter</td>
      <td>info:eu-repo/semantics/bookPart</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>Conference Paper/Proceeding/Abstract</td>
      <td>info:eu-repo/semantics/conferenceObject</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>Journal Article/Review</td>
      <td>info:eu-repo/semantics/article</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>Manual/Guide</td>
      <td>info:eu-repo/semantics/technicalDocumentation</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>Monograph</td>
      <td>info:eu-repo/semantics/book</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>Policy Briefing Report</td>
      <td>info:eu-repo/semantics/report</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>Technical Report</td>
      <td>info:eu-repo/semantics/report</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>Technical Standard</td>
      <td>info:eu-repo/semantics/other</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>Thesis</td>
      <td>info:eu-repo/semantics/other</td>
      <td>OpenAIRE provides:</p>
        <ul>
          <li>info:eu-repo/semantics/bachelorThesis</li>
          <li>info:eu-repo/semantics/masterThesis</li>
          <li>info:eu-repo/semantics/doctoralThesis</li>
        </ul>
        <p>but since it is impossible to select from these based on the RIOXX term, it would be potentially misleading to use one of these OpenAIRE terms</td>
    </tr>
    <tr>
      <td>Other</td>
      <td>info:eu-repo/semantics/other</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>Consultancy Report</td>
      <td>info:eu-repo/semantics/report</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>Working Paper</td>
      <td>info:eu-repo/semantics/workingPaper</td>
      <td>&nbsp;</td>
    </tr>
  </tbody>
</table>

<br />
<br />

<h2>Vocabulary mapping: Publication Versions</h2>
<table class="table table-condensed table-striped sorted-table">
  <thead>
    <tr>
      <th>RIOXX</th>
      <th>OpenAIRE</th>
      <th>Notes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>AO = Author&#39;s Original</td>
      <td>info:eu-repo/semantics/authorVersion</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>SMUR = Submitted Manuscript Under Review</td>
      <td>info:eu-repo/semantics/submittedVersion</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>AM = Accepted Manuscript</td>
      <td>info:eu-repo/semantics/acceptedVersion</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>P = Proof</td>
      <td></td>
      <td>There is no eqivalent OpenAIRE term for this.</td>
    </tr>
    <tr>
      <td>VoR = Version of Record</td>
      <td>info:eu-repo/semantics/publishedVersion</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>CVoR = Corrected Version of Record</td>
      <td>info:eu-repo/semantics/updatedVersion</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>EVoR = Enhanced Version of Record</td>
      <td>info:eu-repo/semantics/updatedVersion</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>NA = Not Applicable (or Unknown)</td>
      <td>info:eu-repo/semantics/updatedVersion</td>
      <td>&nbsp;</td>
    </tr>
  </tbody>
</table>