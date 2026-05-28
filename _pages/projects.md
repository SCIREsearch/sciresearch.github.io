---
layout: page
title: Research
permalink: /projects/
nav: true
nav_order: 1
horizontal: true
---

Language is more than a tool for description &mdash; it persuades and promulgates; it deflects, distorts, and deceives; it constructs our realities as readily as it corrupts them. SCIRE (Latin: _to know_) studies the pragmatic dimensions of language: not what words denote, but what they do — how they maneuver, manipulate, and manufacture the appearance of credibility, consensus, and legitimacy in discourse. This is a central problem of language comprehension. “Meaning” is inseparable from context, intent, and social embedding, and computational systems that ignore this systematically fail at tasks where it matters most: detecting misinformation and manipulation, auditing regulatory compliance, and retrieving reliable information for patient-centric clinical insights.

Our research develops the computational and theoretical machinery to make pragmatic language analysis tractable and consequential. We work across four interconnected areas — <span style="color: #3A5C7F; font-weight: 700;">pragmatic language analysis</span>, <span style="color: #D66037; font-weight: 700;">trustworthy AI and information integrity</span>, <span style="color: #6EA53A; font-weight: 700;">privacy and regulatory compliance</span>, and <span style="color: #EE9D3B; font-weight: 700;">biomedical NLP and healthcare AI</span> &mdash; united by the conviction that the most important AI systems are those designed to support socially-embedded, trustworthy decision-making rather than to optimize narrowly for benchmark performance.

<div class="scire-strip-wrap">
  <div class="scire-stats">
    <div class="scire-stat">
      <span class="scire-stat-value">$1.059M</span>
      <span class="scire-stat-label">in research funding</span>
    </div>
    <div class="scire-stat">
      <span class="scire-stat-value">4</span>
      <span class="scire-stat-label">doctoral researchers</span>
    </div>
    <div class="scire-stat">
      <span class="scire-stat-value">43</span>
      <span class="scire-stat-label">M.S. students</span>
    </div>
    <div class="scire-stat">
      <span class="scire-stat-value">1</span>
      <span class="scire-stat-label">open dataset resource</span>
    </div>
    <div class="scire-stat">
      <span class="scire-stat-value">3</span>
      <span class="scire-stat-label">collaborating universities</span>
    </div>
  </div>
  <div class="scire-collab-footer">
    <span class="scire-collab-label">Collaborating universities —</span>
    <span class="scire-collab-name">New Jersey Institute of Technology</span>
    <span class="scire-collab-sep">·</span>
    <span class="scire-collab-name">Colorado State University, Fort Collins</span>
    <span class="scire-collab-sep">·</span>
    <span class="scire-collab-name">University of Calgary</span>
  </div>
  <div class="scire-collab-footer scire-ug-footer">
    <span class="scire-collab-label">+ 22 undergraduate researchers from Computer Science, Linguistics, and Psychology.</span>
  </div>
  <br>
  <p class="scire-highlight">Student involvement in research is a core value of our group at SCIRE. Of the M.S. and undergraduate students who have worked in our group, <b>19</b> have co-authored peer-reviewed publications at venues including ACL, EMNLP, IEEE ICHI, and others.</p>
</div>


#### Pragmatic Language Analysis

We frame subtle discourse phenomena &mdash; whataboutism, deflection, rhetorical reframing, figurative language &mdash; as computationally identifiable pragmatic language acts that resist resolution by semantics alone. Detecting that a claim is technically true, for instance, tells us nothing about whether it has been deployed to deceive. Our work demonstrates both how existing AI benchmarks fail to capture implicit meaning and conversational maneuvering, and how to move past those failures &mdash; by modeling the strategic intent behind language use rather than the propositional content of the utterance and it linguistic context.

{% assign section_projects = site.projects | where: "research_area", "pragmatic-language" | sort: "importance" %}
{% if section_projects.size > 0 %}
<div class="projects">
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in section_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
</div>
{% endif %}


#### Trustworthy AI and Information Integrity

SCIRE's work on information integrity predates the current wave of interest in AI-generated misinformation by half a decade. Before the term "hallucination" entered the AI lexicon, we were studying **deceptive support** &mdash; the strategic use of the _perception_ of evidence to construct a misleading picture of credibility and reality &mdash; as well as latent deception signals in stylometric patterns in digital writing. From that foundation, we moved to the cross-genre and cross-lingual architecture of misinformation: the same health claim appears differently in a news article, a tweet, and a scientific abstract; and automated systems that fail to map these changes will fail in real-world deployment.

{% assign section_projects = site.projects | where: "research_area", "trustworthy-ai" | sort: "importance" %}
{% if section_projects.size > 0 %}
<div class="projects">
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in section_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
</div>
{% endif %}


#### Privacy and Regulatory Compliance

Legal and regulatory documents are among the most consequential uses of natural language, yet they remain among the least
studied from a computational perspective. Privacy policies, app permission disclosures, and data-use agreements are written
in natural language &mdash; but they must be evaluated against the formal requirements of laws that vary by jurisdiction,
by sector, and by enforcement regime. Our research treats this mismatch as a language understanding problem, and asks:
_does the language of this document do what its authors claim, and does it comply with the legal language it is bound by?_

This research operates at two scales. At the application level, we develop NLP models that automatically infer what data a
mobile app collects and uses from its textual description and permission declarations, and then test whether that behavior
is consistent with what the app actually does<!-- [PST 2025] -->. At the jurisdictional level, we study how privacy laws across
multiple nations &mdash; from GDPR in Europe to DPDPA in India &mdash; construct and enforce different notions of data
protection, and what those differences mean for globally deployed software and services<!-- sharma2026codaspy -->. The
latter is not merely a legal or policy question: it is a natural language inference problem at scale, because the meanings
of "consent", "sensitive data", and "legitimate interest" shift materially across legal corpora.

{% assign section_projects = site.projects | where: "research_area", "privacy-compliance" | sort: "importance" %}
{% if section_projects.size > 0 %}
<div class="projects">
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in section_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
</div>
{% endif %}


#### Biomedical NLP and Healthcare AI

Much of the knowledge that could improve patient outcomes already exists &mdash; in clinical notes,
imaging reports, medication records, and research literature written for human readers and largely
inaccessible to automated systems. The central challenge is not producing more data, but extracting
actionable insights from the language in which clinical data lives, reliably enough to inform patient
care at scale. Our work in this area is pursued under the umbrella of CLAP (Computational Linguistics
and AI for Patients) since 2014, and spans patient-centered AI for adverse drug event detection,
clinical note analysis, medication event extraction, radiology report summarization, and kidney
ultrasound interpretation for chronic kidney disease risk prediction. This research is conducted in
close collaboration with clinicians and medical researchers at the Renaissance School of Medicine in
Stony Brook University.

{% assign section_projects = site.projects | where: "research_area", "biomedical-nlp" | sort: "importance" %}
{% if section_projects.size > 0 %}
<div class="projects">
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in section_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
</div>
{% endif %}


> **Socially-Grounded AI**
> <br>
> Across all of this research, we treat language comprehension as a fundamentally social act. Meaning is not
> a property of a text alone &mdash; it emerges from the creator's intent, the audience's expectations, and
> the broader socio-economic context in which both are situated. This framing commits us to something important:
> building AI systems that are not merely accurate in the statistical sense, but that are _interpretable_ in
> terms of the social dynamics they model. We work at the intersection of computational linguistics, machine
> learning, sociology, and psychology not because breadth is an end in itself, but because the problems we care
> about cannot be solved from within any one of these disciplines alone.
{: .block-tip}
