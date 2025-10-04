---
layout: page
title: Tracking Semantic Changes in Medical Information
img: assets/img/tracking-project-card-img.png
sponsor_img: assets/img/nsf-logo.png
importance: 1
category: Current Projects
related_publications: false
---

---

<h6 class="project-sponsor">This research is funded by the <strong>Secure & Trustworthy Cyberspace (SaTC)</strong> program of the  <strong>U.S. National Science Foundation (NSF)</strong></h6>
<h6 class="project-sponsor">
  <span style="font-weight: 400; font-size: 0.8rem;">
    <a href="https://www.nsf.gov/awardsearch/showAward?AWD_ID=1834597">SES-1834597</a>
  </span>
  <span style="font-weight: 800;">&nbsp;|&nbsp;</span>
  <span style="font-weight: 400; font-size: 0.8rem;">
    05.2018 - 03.2022
  </span>
</h6>


> [**Ritwik Banerjee**](https://www.ritwikbanerjee.com) \| Principal Investigator
> <br>
> Chaoyuan Zuo, Ph.D. &nbsp;&rArr;&nbsp;  Faculty @ School of Journalism & Communication, Nankai University (China)
> <br>
> Noushin Salek Faramarzi, Ph.D. &nbsp;&rArr;&nbsp; Natural Language Understanding @ Boeing
> <br>
> Kritik Mathur, M.S. &nbsp;&rArr;&nbsp; Software Engineer @ Amazon
> <br>
> Dhruv Kela, M.S. &nbsp;&rArr;&nbsp; Software Engineer @ DigitalOcean
> <br>
> Narayan Acharya, M.S. &nbsp;&rArr;&nbsp; Research Engineer @ dmetrics, Inc.
> <br>
> Ayla Karakas, B.S. (Linguistics) Ph.D., &nbsp;&rArr;&nbsp; Computational Linguistics @ Yale
> <br>
> Qi Zhang, B.S. &nbsp;&rArr;&nbsp; MS, University of California San Diego
{: .block-tip }

> ##### Collaborators
> [**Indrakshi Ray**](https://www.cs.colostate.edu/~iray), Colorado State University
> <br>
> [**Hossein Shirazi**](https://www.hosseinshirazi.info/), San Diego State University
> <br>
> Fateme Hashemi Chaleshtori, M.S., Colorado State University
> <br>
> Sina Mahdipour Saravani, M.S., Colorado State University
{: .block-warning}

---

#### Overview

In this groundbreaking research, our team tackled a major issue plaguing today's digital world: **how medical information can change as it moves from research papers to news articles and social media posts**. Changes in the meaning of information as it passes through cyberspace can mislead those who access the information, making it crucial to understand these transformations.

By focusing on subtle shifts in meaning -- like oversimplification or selective reporting -- the project reveals how even well-cited and reputable medical news can mislead readers. Instead of imposing an external `true/false` label on information, this research looks into a series of changes within the news coverage itself that gradually lead to a deviation from the original claims. Our team explored information change in narratives, including semantic changes and nuances, or selective emphasis of related information.

Using advanced information retrieval (IR) and deep neural network models, we studied these shifts *without relying on human judgment*, marking the first-ever AI-driven cross-genre analysis of health misinformation. This approach went beyond contemporary methods limited to binary labels and avoided the potential biases imposed by external fact-checkers. One major finding showed that **at least 1% of social media posts citing reputable news sources used those citations deceptively, creating false trust**.

Our research developed new datasets and algorithms to identify and categorize medical information that remains true to the original meaning or undergoes distortion. Identifying important differences between original articles and news stories is a challenging venture with a significant risk-reward tradeoff, but the research produced valuable tools for verifying health-related claims across genres and trained the next generation of researchers.

**Broader impacts:** This research offers benefits to the research community by making novel contributions to understanding temporal changes in natural language information, as well as social benefits in the form of improved informational tools. For the medical domain in particular, understanding temporal distortions and deviations from actual medical findings can reduce occurrences of harmful health choices, for instance, by embedding the research outcomes in news, social media, or search engines. Through this project, we highlight how AI can help protect us from misleading information in health-related news and social media *without reliance on external sources of expertise for their opinions*.

---

As a first step in this direction, we focused on identifying what information is worth verifying, and developed a hybrid method comprising heuristics and supervised learning to identify "check-worthy" information {% cite zuo2018hybrid %}. Our approach achieved the best state-of-the-art detection, as measured by several metrics. An expansion on this work was invited to the CLEF 2019 conference {% cite zuo2019tocheck %}.

Next, we looked into how healthcare information is first presented in research literature, and then in newswires for general readership. We developed a novel dataset of 5,034 news articles paired with the research abstracts of the work being mentioned, and explored how to identify identical or near-identical content expressed in vastly different syntax and vocabulary. For this, we took a two-step approach: (1) select the most relevant candidates from a collection of 222,000 research abstracts, and (2) re-rank this list of most relevant candidates. We compared the classical approach of information retrieval (IR) using BM25 with more recent transformer-based models, and find that cross-genre medical IR is a viable task, but incorporating domain-specific knowledge is crucial for its success {% cite zuo2020querying %}.

Through the course of this project, we observed that the complex nature of medical misinformation can be attributed largely to two phenomena. First, (mis)information propagates across multiple distinct genres &mdash; from research literature to newswires to social media, where each genre has its own linguistic properties and pragmatic hurdles to overcome. Second, a large amount of information amounts to paltering, or what is often called "less than lying". We have pursued scientific investigations in both directions.

##### (Mis)information propagation across genres

In the former, we looked into the phenomenon of linguistic transformations that happen when medical information transitions from specialized research literature into news intended for wider readership. This transition makes the information vulnerable to misinterpretation, misrepresentation, and incorrect attribution, all of which may be difficult to identify without adequate domain knowledge and may exist even in the presence of explicit citations. Moreover, news articles seldom provide a precise correspondence between a specific claim and its origin, making it harder to identify which claims, if any, reflect the original findings. For instance, an article stating “Flagellin shows therapeutic potential with H3N2, known as Aussie Flu.” contains two claims (“Flagellin ... H3N2,” and “H3N2, known as Aussie Flu”) that may be true or false independent of each other, and it is prima facie unclear which claims, if any, are supported by the cited research. We developed a corpus of sentences from medical news along with the sources from peer-reviewed medical research journals these news articles cite. Then, we used this corpus to study what a general reader perceives to be true, and how to verify the scientific source of claims. Unlike existing corpora, this captures the metamorphosis of information across two genres with disparate readership and vastly different vocabularies and presents the first empirical study of health-related fact-checking across them {% cite zuo2022beyond %}.

We ventured further into the cross-genre propagation of misinformation and the perception of truth. For this part of our research, we collaborated with a team led by Dr. Indrakshi Ray at Colorado State University, Fort Collins. As prior research has often demonstrated, social media posts often leverage the trust readers have in prestigious news agencies and cite news articles as a way of gaining credibility. It is not, however, always the case that the cited article supports the claim being upheld in the social media post. In other words, the post makes it "look" like the claim originates from a credible source, but it really does not! We develop a cross-genre ad hoc information retrieval model to identify whether the information in a Twitter post is, indeed, supported by the news article it cites. This leg of our work rests on a large corpus of 46.86 million Twitter posts about COVID-19, and is divided into two tasks: (i) development of models to detect Tweets containing claim and worth to be fact-checked and (ii) verifying whether the claims made in a Tweet are supported by the newswire article it cites. Unlike previous studies that detect unsubstantiated information by post hoc analysis of the patterns of propagation, our approach is capable of identifying deceptive support before the misinformation begins to spread. Among our chief findings is the observation that among the posts that contain a seemingly factual claim while citing a news article as supporting evidence, at least 1% include a citation intended to deceive the reader {% cite zuo2022seeing %}.

##### Less than lying

The latter consists of selective reporting, non-disclosure of conflicts of interests, disease-mongering, etc. These manifold attributes make the automatic detection of medical misinformation a daunting challenge, and has so far only been explored by journalists and healthcare professionals in purely qualitative studies. We delved into a significantly more complex multi-class classification task to test whether medical news articles (most of which are not considered "fake" by any existing fact-checking system) actually satisfy criteria deemed important by medical experts and healthcare journalists (as far as misinformation is concerned). We collected a corpus of 1,119 health news paired with systematic reviews, where each review has six criteria essential to the accuracy of medical news. Our experiments compared classical token-based approaches with the more recent transformer-based models, and found that detecting qualitative lapses is an extremely challenging task with direct ramifications in misinformation. Moreover, it is an important direction to pursue beyond assigning True or False labels to short claims {% cite zuo2021empirical %}.

{% cite saravani2021investigation %}

{% cite banerjee2021diagnosis %}

---

#### Publications
> {% reference zuo2018hybrid %}
> &nbsp;&nbsp;&nbsp;&nbsp;
> [<i class="fas fa-file-pdf"></i>](/assets/pdf/zuo2018hybrid-clef.pdf)
> <br><br>
> {% reference zuo2019tocheck %}
> &nbsp;&nbsp;&nbsp;&nbsp;
> [<i class="fas fa-file-pdf"></i>](/assets/pdf/zuo2018tocheck-clef.pdf)
> <br><br>
> {% reference zuo2020querying %}
> &nbsp;&nbsp;&nbsp;&nbsp;
> [<i class="fas fa-file-pdf"></i>](/assets/pdf/zuo2020querying.pdf)
> <br><br>
> {% reference zuo2022beyond %}
> &nbsp;&nbsp;&nbsp;&nbsp;
> [<i class="fas fa-file-pdf"></i>](/assets/pdf/zuo2022beyond-journal.pdf)
> <br><br>
> {% reference zuo2022seeing %}
> &nbsp;&nbsp;&nbsp;&nbsp;
> [<i class="fas fa-file-pdf"></i>](/assets/pdf/zuo2022seeing-journal.pdf)
> <br><br>
> {% reference zuo2021empirical %}
> &nbsp;&nbsp;&nbsp;&nbsp;
> [<i class="fas fa-file-pdf"></i>](/assets/pdf/zuo2021empirical.pdf)
> <br><br>
> {% reference saravani2021investigation %}
> &nbsp;&nbsp;&nbsp;&nbsp;
> [<i class="fas fa-file-pdf"></i>](/assets/pdf/saravani2021investigation.pdf)
> <br><br>
> {% reference banerjee2021diagnosis %}
> &nbsp;&nbsp;&nbsp;&nbsp;
> [<i class="fas fa-file-pdf"></i>](https://par.nsf.gov/servlets/purl/10341221)
{: .block-references }
  
<br>
<br>
<span style="float: right; font-weight: 200; font-size: 0.75rem;"><i>This project page is hosted and maintained by the principal investigator, [Dr. Ritwik Banerjee](https://www.ritwikbanerjee.com).</i></span>
