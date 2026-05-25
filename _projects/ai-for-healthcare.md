---
layout: page
title: CL4PHealth | Clinical Language Processing for Healthcare # title on the card
heading: Clinical Language Processing for Healthcare | CL4PHealth # heading for the project page
description: 2014 - 2015 <br> 2022 - 2025
research_area: biomedical-nlp
img: assets/img/cl4phealth-card-img.png
sponsor_img: assets/img/suny-logo.png
importance: 3
category: Research Projects
related_publications: false
---

---

<h6 class="project-sponsor">
This is not a single project, but an amalgamation of multiple projects in our area of interest.
<br>
This research is partly funded by a <strong>SUNY Small Team Multidisciplinary Award</strong> and a <strong>SUNY Seed Grant</strong>.
</h6>

> [**Ritwik Banerjee**](https://www.ritwikbanerjee.com) \| Research Assistant Professor, Computer Science <br>
> Chenlu Wang \| Research Assistant, Computer Science <br>
> Noushin Salek Faramarzi, Ph.D. &nbsp;&rArr;&nbsp; Natural Language Understanding @ Boeing <br>
> Akanksha Dara, M.S. &nbsp;&rArr;&nbsp; Software Engineer, Apple Inc. <br>
> Meet Patel, M.S. &nbsp;&rArr;&nbsp; Software Engineer, Yahoo <br>
> S. Harika Bandarupally, M.S. &nbsp;&rArr;&nbsp; Software Engineer, Meta <br>
{: .block-tip }

> ##### Collaborators
> [**Yejin Choi**](https://hai.stanford.edu/people/yejin-choi) \| Professor, Computer Science, Stanford University <br>
> [**I. V. Ramakrishnan**](https://www.cs.stonybrook.edu/people/faculty/ivramakrishnan) \| Professor, Computer Science <br>
> **Mark C. Henry** \| Professor and Chair Emeritus, Emergency Medicine <br>
> **Matthew Perciavalle** \| Clinical Pharmacist, Emergency Medicine <br>
> [**Farrukh M. Koraishy**](https://renaissance.stonybrookmedicine.edu/medicine/nephrology/faculty_research/koraishy_research) \| Clinical Professor, Nephrology
{: .block-warning}

---

A problem in healthcare is that in spite of the recent focus on precision medicine, much of the relevant data is not patient-specific, and thus, corroborating relevant information and discarding the rest remains the manual endeavor of clinicians. In the first span of this research, from 2014-2015, we recognized this as a rather complex problem, with several aspects to it such as laboratory tests, prescription drugs, diet, etc. Thus, we developed AI-driven systems that can distill patient-specific information from large amounts of natural language data as well as structured databases. This has led to automatic recommendation of the most relevant laboratory tests for a patient, depending on the precise circumstances {% cite banerjee2014automated %}, and personalized identification of adverse drug reactions and attribution of patient's symptoms to their drug regimen {% cite banerjee2015patient %}.

By 2022, the landscape of natural language processing had transformed dramatically with the advent of transformer-based architectures. We pivoted to leverage these advances, investigating how modern deep learning models could better understand the semantic relationships within clinical documentation. Our work on semantic textual similarity in clinical notes demonstrated that transformer models pretrained on clinical text, when combined with medical ontologies like [MeSH](https://www.nlm.nih.gov/mesh/meshhome.html), could achieve strong performance without requiring extensive additional clinical training data {% cite salekfaramarzi2022combining %}. This represented a shift from feature-based extraction toward contextualized understanding of medical language in a manner that combined deep learning with interpretable structures.

We then applied these transformer-based approaches to a more specific and practically challenging problem: extracting medication events from unstructured clinical narratives. Accurate medication history is fundamental to patient care, yet the complexity of how this information appears in clinical notes had made automated extraction difficult. By systematically evaluating various pretrained language models and incorporating domain-specific training with careful data augmentation, we achieved notable improvements in medication event detection {% cite salekfaramarzi2023context %}. This work underscored an important lesson: *even the most sophisticated models require thoughtful preprocessing and domain adaptation to handle the nuances of medical documentation*.

Most recently, we extended our NLP methodology to an entirely different clinical domain: the analysis of kidney ultrasound reports for chronic kidney disease detection. Here, we returned to a fundamental question about model design &mdash; whether word-level or sentence-level approaches better capture diagnostic features. Interestingly, we found that the simpler word-level lexical models outperformed sentence-level analysis for identifying increased kidney echogenicity, a key marker of chronic kidney disease. When applied across over a thousand reports, this approach revealed that bilaterally increased echogenicity was the strongest predictor of chronic kidney disease, with nearly eight-fold increased odds. Through this work, we illustrated how NLP can transform descriptive imaging reports into structured, actionable risk assessments, potentially enabling earlier detection and intervention at scale across healthcare systems {%cite wang2025natural%}.

---

#### Publications
> {% reference banerjee2014automated %}
> &nbsp;&nbsp;&nbsp;&nbsp;
> [<i class="fas fa-file-pdf"></i>](/assets/pdf/banerjee2014automated.pdf)
> <br>
> {% reference banerjee2015patient %}
> &nbsp;&nbsp;&nbsp;&nbsp;
> [<i class="fas fa-file-pdf"></i>](/assets/pdf/banerjee2015patient.pdf)
> <br>
> {% reference salekfaramarzi2022combining %}
> &nbsp;&nbsp;&nbsp;&nbsp;
> [<i class="fas fa-file-pdf"></i>](/assets/pdf/salekfaramarzi2022combining.pdf)
> <br>
> {% reference salekfaramarzi2023context %}
> &nbsp;&nbsp;&nbsp;&nbsp;
> [<i class="fas fa-file-pdf"></i>](/assets/pdf/salekfaramarzi2023context.pdf)
> <br>
> {% reference wang2025natural %}
> &nbsp;&nbsp;&nbsp;&nbsp;
> [<i class="fas fa-file-pdf"></i>](/assets/pdf/wang2025natural-renalfailure.pdf)
{: .block-references }
  
---

<br>
<span style="float: right; font-weight: 200; font-size: 0.75rem;"><i>This project page is hosted and maintained by the principal investigator, [Dr. Ritwik Banerjee](https://www.ritwikbanerjee.com).</i></span>
