---
layout: page
title: Propaganda, Fallacies, and Media Integrity
heading: Propaganda, Fallacies, and Media Integrity
description: Detecting propaganda and reasoning fallacies in online media
research_area: trustworthy-ai
img: assets/img/project-card-images/propaganda-fallacies-integrity-card-img.png
sponsor_imgs: assets/img/ai3_logo.png
importance: 2
category: Research Projects
related_publications: false
---

> <div class="project-sponsor">
>   This research has been supported in part by the <strong>AI Innovation Institute (AI3)</strong> at Stony Brook University.</div>
> <div class="project-sponsor">
>   <a href="https://www.stonybrook.edu/commcms/provost/about/_communications/_2025_ai_seed_grant_winners.php">AI3 Seed Grant</a>
>   (01.2025 - 06.2026)
> </div>
{: .block-preferences }

---

> [**Ritwik Banerjee**](https://www.ritwikbanerjee.com), Principal Investigator <br>
> [**Ruobing Li**](https://www.stonybrook.edu/commcms/journalism/about/ruobing_li.php), School of Communication and Journalism,
> Co-Investigator <br>
> Chenlu Wang, Doctoral Researcher &nbsp;&rarr;&nbsp; Research Scientist, Meta <br>
> Weimin Lyu, Doctoral Researcher &nbsp;&rarr;&nbsp; Applied Scientist, Amazon <br>
> Parth Thapliyal, M.S. Researcher <br>
> Jelwin Rodrigues, M.S. Researcher <br>
> Abhishek Kalugade, M.S. Researcher <br>
> Harsh Gupta, M.S. Researcher <br>
> Taisiia Sabadyn, Undergraduate Researcher <br>
> Ritesh Sunil Chavan, Undergraduate Researcher <br>
> Samridh Samridh, Undergraduate Researcher
{: .block-tip }

> ##### Collaborators
> Dikshya Mohanty, Doctoral Researcher
> <br>
> Chaoyuan Zuo, Lecturer (tenure-track), School of Journalism & Communication, Nankai University
{: .block-warning }

---

Large language models have achieved striking performance on NLP benchmarks while
failing systematically at a class of tasks that requires pragmatic competence rather than
surface-level semantic matching: detecting propaganda techniques and fallacious argumentation
in online discourse. This is not a minor gap. Propaganda operates through framing, selective
emphasis, and emotional manipulation — none of which leaves a straightforward lexical
signature. Fallacies like whataboutism, appeal to majority, and false causality derive their
persuasive power precisely from their resemblance to valid argument forms. A model that cannot
distinguish the structure of an argument from its surface appearance will miss both, allowing
complex misinformation to pass undetected.

This project investigates the computational roots of this failure and develops targeted
responses. It is organized around three objectives.

#### Diagnosing LLM Limitations

The first objective characterizes *why* current models fail, not just *that* they fail.
Using a multi-pronged diagnostic approach — thematic analysis of error patterns, adversarial
testing with near-minimal pairs, and attention mechanism analysis — we map the specific
aspects of pragmatic context that transformer-based models are unable to integrate. Prior
work by the PI on whataboutism detection demonstrated that cross-attention weights carry
recoverable signals about discourse-level intent that standard classification heads do not
exploit; this project extends that diagnostic lens to the broader landscape of propaganda
techniques and argumentation fallacies, including their co-occurrence, which amplifies
persuasive power in ways that models trained on isolated instances cannot recognize.

#### Developing Improved Detection Models

The second objective develops detection models informed by these diagnostics. The key
methodological insight is that sociocultural context external to a single document —
captured through cross-document discourse signals from social media commentary and
adjacent reporting — provides the pragmatic grounding that in-document context alone
cannot supply. Preliminary results show that integrating this broader context through
parametric methods and attention-based distance metrics outperforms retrieval-augmented
generation systems while requiring substantially less training data. The class distillation
framework developed in parallel work provides an efficient training paradigm particularly
suited to the small-target-class structure of propaganda and fallacy detection tasks {% cite
wang2025class %}.

#### A Corpus for Narrative Divergence and Information Integrity

Understanding propaganda and information distortion at scale requires corpora that capture
how the same events are narrated across different national media ecosystems — not just
within a single genre or language. We constructed **<span style="font-variant: small-caps;">dnipro</span>**
(**D**iverse **N**arratives and **I**nternational **P**erspectives on the **R**usso-Ukrainian
**O**ffensive), a longitudinal, multinational, and multilingual corpus spanning 31 months of
news coverage of the Russo-Ukrainian war, drawn from sources in the United States, United Kingdom,
Ukraine, Russia, and China, in English, Russian, and Mandarin Chinese {% cite mohanty2026longitudinal %}.
<span style="font-variant: small-caps;">dnipro</span> is released on Zenodo as a public resource<sup>1</sup>
and supports research on narrative divergence, counter-narrative analysis, and the cross-national
propagation of contested claims &mdash; questions that are at the heart of computational approaches
to propaganda analysis and information integrity.

> <sup>1</sup> &nbsp; <span style="font-size:0.75rem;">Mohanty, D., Sabadyn, T., Rodrigues, J.,
> Wang, C., Kalugade, A., &amp; Banerjee, R. (2026). Diverse Narratives and International
> Perspectives on the Russo-Ukrainian Offensive (DNIPRO) (Version v1) [Data set]. Zenodo.
> doi: <a href="https://doi.org/10.5281/zenodo.18470677">10.5281/zenodo.18470677</a></span>
{: .block-references }


#### Scientific Discourse and Cross-Genre Verification

A parallel thread addresses misinformation propagation through the scientific literature
pipeline, where peer-reviewed findings are translated into journalism and social media under
pressures that distort both accuracy and emphasis. We developed and evaluated systems
for the CLEF CheckThat! 2025 shared task, which targets scientific claim verification by
bridging social media discourse, science journalism, and the primary scientific literature
{% cite thapliyal2025 %}. Complementary work on LLM-driven biomedical named entity
recognition {% cite gupta2025scire %} contributes to the information extraction infrastructure
that underlies cross-genre claim verification, while also probing the capabilities and
limitations of LLMs in specialized biomedical domains.

#### Media Literacy and Education

The third objective translates research findings into educational materials for students in
journalism and communication — populations that are methodologically sophisticated but
underserved by technical AI literacy curricula. Working with the School of Communication
and Journalism, the Center for News Literacy, and the Alan Alda Center for Communicating
Science, the project develops lecture modules and case studies integrating these findings into
core courses and outreach programs, contributing to a broader public understanding of how
AI can and cannot be used to identify manipulation in media.

---

#### Publications

> {% reference mohanty2026longitudinal %}
> &nbsp;&nbsp;&nbsp;&nbsp;
> [<i class="fas fa-file-pdf"></i>](/assets/pdf/mohanty2026longitudinal.pdf)
> <br><br>
> {% reference wang2025class %}
> &nbsp;&nbsp;&nbsp;&nbsp;
> [<i class="fas fa-file-pdf"></i>](/assets/pdf/wang2025class.pdf)
> <br><br>
> {% reference thapliyal2025 %}
> &nbsp;&nbsp;&nbsp;&nbsp;
> [<i class="fas fa-file-pdf"></i>](/assets/pdf/thapliyal2025scire-clef.pdf)
> <br><br>
> {% reference gupta2025scire %}
> &nbsp;&nbsp;&nbsp;&nbsp;
> [<i class="fas fa-file-pdf"></i>](/assets/pdf/gupta2025scire.pdf)
{: .block-references }

---

<br>
<span style="float: right; font-weight: 200; font-size: 0.75rem;"><i>This project page is
hosted and maintained by the principal investigator,
[Dr. Ritwik Banerjee](https://www.ritwikbanerjee.com).</i></span>
