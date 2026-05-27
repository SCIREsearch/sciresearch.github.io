---
layout: page
title: Contraceptive Misinformation on Social Media
heading: Contraceptive Misinformation on Social Media
description: Belief-driven distortion of contraceptive narratives across platforms
research_area: trustworthy-ai
img: assets/img/project-card-images/contraceptive-misinformation-card-img.png
sponsor_img: assets/img/sfp-logo.svg
importance: 1
category: Research Projects
related_publications: false
---

> <div class="project-sponsor">
>   This research is funded by the <strong>Society for Family Planning</strong>.
> </div>
> <div class="project-sponsor">
>    <a href="https://societyfp.org/awarded_grants/sfp19-mdi2/">SPF19-MDI2</a>
>    (01.2026 - 12.2027)
> </div>
{: .block-preferences }

---

> [**Ritwik Banerjee**](https://www.ritwikbanerjee.com), Principal Investigator
{: .block-tip }

---

Contraceptive misinformation is not a monolithic phenomenon amenable to simple keyword
detection or binary fact-checking. It propagates through polarized epistemic networks &mdash;
faith-based abstinence communities, wellness conspiracy ecosystems, reproductive justice
advocates &mdash; each with its own rhetorical vocabulary, internal amplification dynamics, and
relationship to scientific evidence. Algorithmic recommendation systems on platforms like
TikTok, YouTube, and Reddit do not merely host this discourse: they actively accelerate it,
by prioritizing engagement over accuracy and surfacing belief-consistent content to users
already predisposed to accept it. The result is a self-reinforcing feedback loop in which
community-specific distortions of contraceptive evidence gain virality precisely because they
confirm what a given audience already believes.

Despite the urgency &mdash; heightened by the post-*Dobbs* landscape in which contraceptive
access and reproductive rights have become actively contested &mdash; the computational research
base is thin. Existing studies rely on broad keyword tracking, which sacrifices specificity,
or on qualitative thematic analyses, which cannot scale to the volume and velocity of social
media discourse. There is no unified computational framework for identifying how rhetorical
strategies vary by community and platform, how algorithmic amplification biases operate at
the level of individual psycholinguistic profiles, or how misinformation propagates and
gains reinforcement as it traverses interconnected platforms. This project addresses these
gaps directly.

##### Community-Specific Rhetorical Models

The first research question asks how distinct communities differentially distort contraceptive
evidence, and which rhetorical strategies most effectively amplify misinformation within each
community's belief network. The computational approach combines frame-semantic parsing
to detect distortion tactics (science-denial framing, false causality claims, evidence
contradiction), discourse analysis grounded in rhetorical structure theory adapted for
multi-platform contexts, and Hawkes process modeling to quantify the self-exciting dynamics
of misinformation diffusion across over one million posts from Twitter/X, YouTube, TikTok,
Reddit, and health forums. Across this corpus, the analysis will produce the first cross-platform
taxonomy of contraceptive misinformation strategies &mdash; a resource enabling community-sensitive
NLP classifiers for real-time detection of community-tailored distortions.

##### Algorithmic Amplification and Belief Reinforcement

The second research question addresses a more subtle mechanism: the extent to which
algorithmic recommendation systems reinforce belief-consistent distortions, and how this
amplification varies by user psycholinguistic profile. Rather than relying on observational
correlational analyses, this work employs a controlled agent-based auditing framework. AI
agents simulating users with diverse psycholinguistic profiles &mdash; varying in cognitive rigidity
and identity-driven motivation, operationalized through linguistic analysis &mdash; interact
organically with platform recommendation systems, generating counterfactual interaction
traces that isolate how algorithmic parameters respond to identical queries from users with
divergent belief profiles. Cross-platform propagation is tracked through temporal knowledge
graphs of shared URLs, capturing how contraceptive misinformation gains reinforcement as
it traverses platforms. Causal inference methods &mdash; specifically Neyman-Rubin counterfactual
modeling &mdash; then establish whether, and how strongly, user psycholinguistic profiles causally
drive increased exposure to belief-distorted content.

##### Equity at the Center

Computational rigor without equity is insufficient for research of this kind. This project
explicitly centers communities that are disproportionately targeted by contraceptive
misinformation &mdash; including youth in abortion-restricted states, low-health-literacy groups,
and LGBTQ+ communities &mdash; by operationalizing vulnerability through intersectional indices
derived from geolocation data, linguistic markers of structural marginalization, and network
isolation metrics. Detection models are trained on data enriched with content from Black,
Latinx, and LGBTQ+ digital communities to ensure recognition of culturally specific
misinformation narratives. All outputs will be released as open-source toolkits designed to
be accessible to under-resourced public health departments, with no requirement for
specialized technical infrastructure.

<small>This is an active project. Publications will be listed here as they become available.</small>

---

<br>
<span style="float: right; font-weight: 200; font-size: 0.75rem;"><i>This project page is
hosted and maintained by the principal investigator,
[Dr. Ritwik Banerjee](https://www.ritwikbanerjee.com).</i></span>
