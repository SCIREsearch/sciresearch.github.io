---
layout: page
title: Research
permalink: /projects/
# description: A growing collection of your cool projects.
nav: true
nav_order: 1
display_categories: [Research Projects]
horizontal: true
---

Language is more than a tool for description &mdash; it persuades and promulgates; it deflects, distorts, and deceives; it constructs our realities as readily as it corrupts them. SCIRE (Latin: _to know_) studies the pragmatic dimensions of language: not what words denote, but what they do — how they maneuver, manipulate, and manufacture the appearance of credibility, consensus, and legitimacy in discourse. This is a central problem of language comprehension. “Meaning” is inseparable from context, intent, and social embedding, and computational systems that ignore this systematically fail at tasks where it matters most: detecting misinformation and manipulation, auditing regulatory compliance, and retrieving reliable information for patient-centric clinical insights.

Our research develops the computational and theoretical machinery to make pragmatic language analysis tractable and consequential. We work across four interconnected areas — **pragmatic language analysis**, **trustworthy AI and information integrity**, **privacy and regulatory compliance**, and **biomedical NLP and healthcare AI** &mdash; united by the conviction that the most important AI systems are those designed to support socially-embedded, trustworthy decision-making rather than to optimize narrowly for benchmark performance.

## Pragmatic Language Analysis

We frame subtle discourse phenomena &mdash; whataboutism, deflection, rhetorical reframing, figurative language {%cite saravani2021investigation %} &mdash; as computationally identifiable pragmatic language acts that resist resolution by semantics alone {%cite wang2025class %}. Detecting that a claim is technically true, for instance, tells us nothing about whether it has been deployed to deceive. Our work demonstrates both how existing AI benchmarks fail to capture implicit meaning and conversational maneuvering, and how to move past those failures &mdash; by modeling the strategic intent behind language use rather than the propositional content of the utterance and it linguistic context {%cite phi2024paying %}.

- {% reference phi2024paying %} &nbsp;&nbsp;&nbsp;&nbsp; [<i class="fas fa-file-pdf"></i>](/assets/pdf/phi2024paying.pdf)
- {% reference wang2025class %} &nbsp;&nbsp;&nbsp;&nbsp; [<i class="fas fa-file-pdf"></i>](/assets/pdf/wang2025class.pdf)
- {% reference saravani2021investigation %} &nbsp;&nbsp;&nbsp;&nbsp; [<i class="fas fa-file-pdf"></i>](/assets/pdf/saravani2021investigation.pdf)


## Trustworthy AI and Information Integrity

SCIRE's work on information integrity predates the current wave of interest in AI-generated misinformation by half a decade. Before the term "hallucination" entered the AI lexicon, we were studying **deceptive support** {%cite zuo2022beyond %}, {%cite zuo2022seeing %} &mdash; the strategic use of the _perception_ of evidence to construct a misleading picture of credibility and reality &mdash; as well as latent deception signals in stylometric patterns in digital writing {%cite feng2012syntactic %}. From that foundation, we moved to the cross-genre {%cite zuo2020querying %}, {%cite zuo2023cross %} and cross-lingual {%cite zuo2025hdcr %} architecture of misinformation: the same health claim appears differently in a news article, a tweet, and a scientific abstract; and automated systems that fail to map these changes will fail in real-world deployment.

- {% reference feng2012syntactic %} &nbsp;&nbsp;&nbsp;&nbsp; [<i class="fas fa-file-pdf"></i>](/assets/pdf/feng2012syntactic.pdf)
- {% reference zuo2020querying %} &nbsp;&nbsp;&nbsp;&nbsp; [<i class="fas fa-file-pdf"></i>](/assets/pdf/zuo2020querying.pdf)
- {% reference zuo2022beyond %} &nbsp;&nbsp;&nbsp;&nbsp; [<i class="fas fa-file-pdf"></i>](/assets/pdf/zuo2022beyond-journal.pdf)
- {% reference zuo2022seeing %} &nbsp;&nbsp;&nbsp;&nbsp; [<i class="fas fa-file-pdf"></i>](/assets/pdf/zuo2022seeing-journal.pdf)
- {% reference zuo2023cross %} &nbsp;&nbsp;&nbsp;&nbsp; [<i class="fas fa-file-pdf"></i>](/assets/pdf/zuo2023cross-adma.pdf)
- {% reference zuo2025hdcr %} &nbsp;&nbsp;&nbsp;&nbsp; [<i class="fas fa-file-pdf"></i>](/assets/pdf/zuo2025hdcr.pdf)


## Privacy and Regulatory Compliance

Legal and regulatory documents are among the most consequential uses of natural language, yet they remain among the least studied from a computational perspective. Privacy policies, app permission disclosures, and data-use agreements are written in natural language — but they must be evaluated against the formal requirements of laws that vary by jurisdiction, by sector, and by enforcement regime. SCIRE treats this mismatch as a language understanding problem. Our work asks: _does the language of this document do what its authors claim, and does it comply with the legal language it is bound by?_

This research operates at two scales. At the application level, we develop NLP models that automatically infer what data a mobile app collects and uses from its textual description and permission declarations, and then test whether that behavior is consistent with what the app actually does [PST 2025]. At the jurisdictional level, we study how privacy laws across multiple nations — from GDPR in Europe to HIPAA in the United States to emerging frameworks in Asia and the Middle East — construct and enforce different notions of data protection, and what those differences mean for globally deployed software and services [CODASPY 2026]. The latter is not merely a legal or policy question: it is a natural language inference problem at scale, because the meaning of "consent," "sensitive data," and "legitimate interest" shifts materially across legal corpora.

This thread of research is supported by the U.S. National Science Foundation's Secure and Trustworthy Cyberspace (SaTC) program.


## Biomedical and Healthcare AI

The single largest gap in modern healthcare is not the absence of medical knowledge — it is the inability to access, interpret, and act on knowledge that already exists, buried in clinical notes, radiology reports, research literature, and patient records that were written for human readers and remain largely inaccessible to automated systems. SCIRE's work in biomedical NLP addresses this gap directly. Our central concern is the _translational problem_: how to move actionable knowledge from the language in which it is recorded to the clinical and research decisions it should inform.

This research has proceeded along two parallel tracks. The first concerns knowledge extraction from clinical text: identifying adverse drug events from electronic health records [ICHI 2014 and ICHI 2015 Best Paper], extracting and contextualizing medication events from unstructured clinical notes [ClinicalNLP 2023], and correlating radiological imaging language with disease diagnosis [Renal Failure 2025]. The second track concerns cross-genre medical claim verification: the same health claim — about a drug, a treatment, a risk — appears across news articles, patient forums, scientific abstracts, and clinical guidelines, and means something different in each. Our work on querying and retrieving medical claims across these genres [EMNLP 2020] and on large-scale biomedical expert finding for claim verification [BIBM 2025] addresses the practical challenge that automated health claim systems must face: the genre of a claim's source is not incidental to its credibility.

This research is conducted in close collaboration with clinicians and medical researchers at Stony Brook University School of Medicine.


## Socially-Grounded AI

Across all of this research, we treat language comprehension as a fundamentally social act. Meaning is not a property of a text alone &mdash; it emerges from the creator's intent, the audience's expectations, and the broader socio-economic context in which both are situated. This framing commits us to something important: building AI systems that are not merely accurate in the statistical sense, but that are _interpretable_ in terms of the social dynamics they model. We work at the intersection of computational linguistics, machine learning, sociology, and psychology not because breadth is an end in itself, but because the problems we care about cannot be solved from within any one of these disciplines alone.


<!-- pages/projects.md -->
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_projects = site.projects | where: "category", category %}
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display projects without categories -->

{% assign sorted_projects = site.projects | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
