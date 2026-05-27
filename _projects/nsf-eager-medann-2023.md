---
layout: page
title: Investigating Medical Data against Privacy Laws
heading: A Framework for Investigating Live Medical Data against Privacy Laws
description: Privacy compliance in health apps and medical information systems
research_area: privacy-compliance
img: assets/img/medann-project-card-img.png
sponsor_img: assets/img/nsf-logo.png
importance: 1
category: Research Projects
related_publications: false
---

> <div class="project-sponsor">
> This research is funded by the <strong>Secure &amp; Trustworthy Cyberspace (SaTC)</strong> program of the <strong>U.S. National Science Foundation (NSF)</strong>
> </div>
> <div class="project-sponsor">
>   <a href="https://www.nsf.gov/awardsearch/showAward?AWD_ID=2335686">CNS-2335686</a>
>   (10.2023 – 09.2025)
> </div>
{: .block-preferences}

> [**Ritwik Banerjee**](https://www.ritwikbanerjee.com), Principal Investigator <br>
> &emsp; Chenlu Wang, Doctoral Researcher &nbsp;&rarr;&nbsp; Research Scientist, Meta <br>
> &emsp; Weimin Lyu, Doctoral Researcher &nbsp;&rarr;&nbsp; Applied Scientist, Amazon
> <br><br>
> [**Indrakshi Ray**](https://www.cs.colostate.edu/~iray), Co-Principal Investigator <br>
> &emsp; Ethan Myers, Doctoral Researcher <br>
> &emsp; Yunik Tamrakar, M.S. Researcher &nbsp;&rarr;&nbsp; Software Engineer, ABC Legal Services
{: .block-tip }

> ##### Collaborators
> [**Lorenzo De Carli**](https://ldklab.github.io/), Associate Professor of Electrical and Software Engineering, University of Calgary <br>
> [**Shantanu Sharma**](https://web.njit.edu/~ss797/), Assitant Professor of Computer Science, New Jersey Institute of Technology <br>
> **Chaoyuan Zuo**, Lecturer (tenure-track), School of Journalism & Communication, Nankai University <br>
{: .block-warning }

---

Digital health systems (mobile apps, clinical databases, health information
services, etc.) operate at the intersection of two demands that NLP is
uniquely positioned to address: regulatory compliance and information
integrity. They must comply with privacy laws that vary by jurisdiction,
sector, and enforcement regime; and they must accurately represent the
scientific evidence they draw on. When either demand is unmet, patients are
exposed to risks they did not consent to — either because an app misrepresents
what it does with their data, or because the health information it surfaces
misrepresents what the science actually says. This project develops the
computational tools and frameworks to detect and measure both classes of failure.

##### Privacy Compliance in Health Applications

Mobile health apps collect some of the most sensitive personal data that
exists &mdash; symptoms, medications, reproductive cycles, mental health
indicators &mdash; and their compliance with the privacy laws governing that
data is difficult to verify at scale. We develop NLP models that automatically
infer what data a health app collects and processes from its textual
description and permission declarations, and test whether that behavior is
consistent with what the app actually does {% cite tamrakar2025harnessing %}.
This work achieves higher accuracy and lower annotation costs than prior
approaches, and provides a practical tool for auditing health app ecosystems
at the platform level.

##### Privacy Laws Across Jurisdictions

The compliance problem is jurisdictional, and not merely technical. A health
app that is GDPR-compliant in Europe may violate DPDPA in India; an app
compliant with both may still fall short of frameworks emerging in the Middle East.
We study how privacy laws across multiple nations (spanning four continents)
construct different, and sometimes incompatible, notions of consent, sensitive
data, and legitimate interest, and what these differences mean for globally
deployed health software and services {% cite sharma2026codaspy %}. This work
frames cross-jurisdictional compliance as a natural language inference problem
at scale: the *meanings* of legal terms shift materially across legal corpora,
and computational models must account for this to be useful in practice.

##### Health Information Integrity

A second thread of this research concerns the scientific accuracy of health
information in digital media. Ensuring that health claims made in apps, news
articles, and social media posts are traceable to legitimate scientific
evidence requires both the ability to identify relevant biomedical expertise
at scale and the ability to detect when a claim has been distorted or
fabricated across language boundaries. We develop a large-scale PubMed-based
retrieval framework for biomedical expert finding, enabling automated
identification of subject-matter experts capable of evaluating specific health
claims {% cite zuo2025biomedical %}.
Complementing this, we develop cross-lingual models for medical misinformation
detection through contrastive claim-evidence reasoning, extending the
verification pipeline beyond English-language sources to multilingual health
discourse {% cite zuo2025hdcr %}. Both systems contribute to the goal of
making the accuracy of health information computationally auditable, not just
manually reviewable.

Our novel and data-efficient training paradigm that may underpin several
improvements to these models (viz., class distillation with Mahalanobis
contrast) is described in detail as part our work on [pragmatic language understanding](/projects/pragmatic-language-understanding/) {% cite wang2025class %}.

##### Broader Impact

This project safeguards user privacy and security in the increasingly
prevalent use of health apps, which handle sensitive personal data. By
addressing regulatory compliance across jurisdictions, improving the
interpretability of legal language in technical contexts, and building tools
for health information verification, the research contributes both to the
protection of individual users and to the broader challenge of making digital
health systems accountable to the scientific and legal standards they operate under.

---

##### Publications

> {% reference sharma2026codaspy %}
> &nbsp;&nbsp;&nbsp;&nbsp;
> (PDF coming soon)
> <br><br>
> {% reference wang2025class %}
> &nbsp;&nbsp;&nbsp;&nbsp;
> [<i class="fas fa-file-pdf"></i>](/assets/pdf/wang2025class.pdf)
> <br><br>
> {% reference zuo2025hdcr %}
> &nbsp;&nbsp;&nbsp;&nbsp;
> [<i class="fas fa-file-pdf"></i>](/assets/pdf/zuo2025hdcr.pdf)
> <br><br>
> {% reference zuo2025large %}
> &nbsp;&nbsp;&nbsp;&nbsp;
> [<i class="fas fa-file-pdf"></i>](/assets/pdf/zuo2025large.pdf)
> <br><br>
> {% reference tamrakar2025harnessing %}
> &nbsp;&nbsp;&nbsp;&nbsp;
> [<i class="fas fa-file-pdf"></i>](/assets/pdf/tamrakar2025harnessing.pdf)
{: .block-references }

---

<br>
<span style="float: right; font-weight: 200; font-size: 0.75rem;"><i>This project page is hosted and maintained by the principal investigator, [Dr. Ritwik Banerjee](https://www.ritwikbanerjee.com).</i></span>
