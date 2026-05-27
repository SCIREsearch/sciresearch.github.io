---
layout: page
title: Pragmatic Language Understanding
heading: Pragmatic Language Understanding
description: Non-Gricean discourse as computationally tractable pragmatic acts
research_area: pragmatic-language
img: assets/img/project-card-images/pragmatic-language-understanding-card-img-2.png
sponsor_imgs:
  - assets/img/nsf-logo.png
  - assets/img/ai3_logo.png
importance: 1
category: Research Projects
related_publications: false
---

> <div class="project-sponsor">
>   This research has been supported in part by the <strong>Secure & Trustworthy Cyberspace (SaTC)</strong> program of the <strong>U.S. National Science Foundation (NSF)</strong> and the <strong>AI Innovation Institute (AI3)</strong> at Stony Brook University.
> </div>
> <div class="project-sponsor">
>    <a href="https://www.nsf.gov/awardsearch/show-award/?AWD_ID=1834597">SES-1834597</a>
>    (05.2018 - 03.2022)
>  <span style="font-weight: 700;">&nbsp;|&nbsp;</span>
>    <a href="https://www.nsf.gov/awardsearch/show-award/?AWD_ID=2335686">CNS-2335686</a>
>    (10.2023 - 09.2025)
>  <span style="font-weight: 700;">&nbsp;|&nbsp;</span>
>    <a href="https://www.stonybrook.edu/commcms/provost/about/_communications/_2025_ai_seed_grant_winners.php">AI3 Seed Grant</a>
>    (01.2025 - 06.2026)
> </div>
{: .block-preferences }

---

> [**Ritwik Banerjee**](https://www.ritwikbanerjee.com), Principal Investigator <br>
> &emsp; Chenlu Wang, Doctoral Researcher &nbsp;&rarr;&nbsp; Research Scientist, Meta <br>
> &emsp; Khiem Phi, Doctoral Researcher <br>
> &emsp; Noushin Salek Faramarzi, Doctoral Researcher &nbsp;&rarr;&nbsp; NLP Researcher, Boeing AI <br>
> &emsp; Weimin Lyu, Doctoral Researcher &nbsp;&rarr;&nbsp; Applied Scientist, Amazon 
{: .block-tip}

##### Collaborators
> [**Indrakshi Ray**](https://www.cs.colostate.edu/~iray), Professor of Computer Science, Colorado State University at Fort Collins
> <br>
> &emsp; Sina Mahdipour Saravani, M.S. Researcher, Colorado State University &nbsp;&rarr;&nbsp; Ph.D. Student, University of Utah
{: .block-warning}

---

#### Overview

Pragmatic language phenomena &mdash; sarcasm, metaphor, sexism &mdash; often share a structural
challenge that standard NLP classification setups handle poorly: the target class is small,
semantically coherent, and precisely defined, but it sits inside a large and highly heterogeneous
background of superficially similar discourse. A model that optimizes for accuracy on such an
imbalanced distribution is learning the semantic patterns instead of the intent-driven phenomena.
The same failure mode appears at the discourse level: whataboutism deploys the topical changes in
the surface forms, but so do ordinary (and sometimes helpful) comparative questions and legitimate
contextualizations. A classifier anchored to semantics alone will systematically conflate a genuine
rhetorical deflection with discourse that merely resembles it. Detecting pragmatic phenomena
requires attending to the pragmatic *function*, not the semantic form.

---

Three lines of work in our group converge on this problem. The first established what does not
help. We investigated NeXtVLAD &mdash; a locally aggregated descriptor architecture borrowed from
computer vision that had produced a striking 93.1% F1 on the FigLang2020 sarcasm detection task,
fourteen points above the next-best system. The result appeared to signal a major architectural
advance for figurative language identification. Controlled ablation experiments, however, demonstrated
that the gain is not statistically significant when proper baselines are held constant, and
the resource-intensive NeXtVLAD component adds no measurable benefit for figurative language
identification {%cite saravani2021investigation %}. The right response to a hard pragmatic task is
not a larger or more elaborate model — it is a more principled training objective.

##### The "Tu Quoque" Fallacy of Argumentation

Whataboutism offered a test case for this principle. The phenomenon &mdash; a rhetorical deflection
that shifts attention rather than addressing the immediate concern &mdash; is pragmatically broader
than the *tu quoque* fallacy, and often distinct from propaganda. But these distinctions had been
systematically conflated in prior work, which treated the "what about" surface pattern as a reliable
proxy for the underlying fallacious argumentation. We introduce two manually annotated datasets
(Twitter/X and YouTube) that make these distinctions explicit, and propose a training method that mines
hard negatives by exploiting attention-weight signals &mdash; targeting the subtle cases where whataboutism
overlaps with (but is not identical to) related rhetorical devices {%cite phi2024paying %}. The
method achieves 4% and 10% absolute improvements over prior state-of-the-art on the two collections,
respectively. The deeper result is methodological: discourse-level signals of _function_, not semantic
forms, are what allow a model to track the *strategic intent* of an utterance rather than its
propositional content.

##### Class Distillation

Our subsequent work on **class distillation (ClaD)** provides the training paradigm that generalizes
this insight across pragmatic language tasks. ClaD is built around two components: a loss function
grounded in Mahalanobis distance that exploits the geometric structure of class distributions rather
than treating all dimensions as equally informative, and an interpretable β-decision algorithm optimized
explicitly for clean separation between the target class and the heterogeneous background of "everything
else" {%cite wang2025class %}. On three benchmark tasks &mdash; sexism, metaphor, and sarcasm detection
&mdash; ClaD with small language models matches or outperforms both standard fine-tuned classifiers and
several large language models with orders of magnitude more parameters.

Ablation experiments confirm that both components are necessary: removing either the Mahalanobis contrast
loss or the β-decision algorithm causes F1 drops of 46–81% depending on the task. For pragmatic language
tasks where the target class has clear distributional structure, explicit geometric modeling of that
manifold is more valuable than raw model scale.

---

#### Publications

> {% reference wang2025class %}
> &nbsp;&nbsp;&nbsp;&nbsp;
> [<i class="fas fa-file-pdf"></i>](/assets/pdf/wang2025class.pdf)
> <br><br>
> {% reference phi2024paying %}
> &nbsp;&nbsp;&nbsp;&nbsp;
> [<i class="fas fa-file-pdf"></i>](/assets/pdf/phi2024paying.pdf)
> <br><br>
> {% reference saravani2021investigation %}
> &nbsp;&nbsp;&nbsp;&nbsp;
> [<i class="fas fa-file-pdf"></i>](/assets/pdf/saravani2021investigation.pdf)
{: .block-references }
  
---

<br>
<span style="float: right; font-weight: 200; font-size: 0.75rem;">This project page is hosted and maintained by the principal investigator, [Dr. Ritwik Banerjee](https://www.ritwikbanerjee.com).</span>
