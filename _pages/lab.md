---
layout: archive
title: "IDEA Lab"
permalink: /lab/
author_profile: true
---

<img
  src="{{ '/images/logo.png' | relative_url }}"
  alt="IDEA LAB logo"
  style="width:500px; max-width:95%; height:auto; display:block; margin: 6px auto 10px auto;"
/>
We are the **IDEA (Impact-Driven Evaluation for AI) Lab** in **NYU Computer Science**, led by Dr. Emily Black. Our research develops methods to measure and mitigate harm AI systems, with a special focus on preventing harm in real-world.

<div class="pub-area-nav">
  <a href="#research">Research</a>
  <a href="#team">Team</a>
  <a href="#open-positions">Open Positions</a>
</div>

### <a id="research"></a>Our research

Our work spans three connected areas:

<details class="lab-area" markdown="1">
<summary>Algorithmic fairness and AI safety</summary>
<div class="lab-area-body" markdown="1">
We build tools, methodologies, and frameworks to measure and prevent harms from AI systems that could negatively impact society. This includes developing evaluation paradigms to identify harms, explainability tools to diagnose why harms arise, and methods for training and selecting models that are both accurate and minimize harms. While our techniques are general and can be applied to a wide range of application areas, we are often inspired by issues such as protecting fair access to high-stakes opportunities like jobs, credit, housing, and health in the age of AI; promoting high-quality and diverse LLM output; and understanding and mitigating instability and arbitrariness in AI systems.

<div class="lab-area-pubs">
{% assign area_pubs = site.data.publications | where: "area", "fairness" | sort: "year" | reverse %}
{% for pub in area_pubs %}
  {% include publication-entry.html %}
{% endfor %}
</div>
</div>
</details>

<details class="lab-area" markdown="1">
<summary>AI and the law / AI governance</summary>
<div class="lab-area-body" markdown="1">
Beyond creating methods to find and prevent harm technically, we study how effective incentive structures, or AI governance strategies, to prevent harm in practice. Towards this goal, we study how to interpret the law in the context of AI systems to understand what requirements companies and other institutions using AI systems in high-stakes may be subject to, how companies can comply with those requirements, and to what extent various AI policy and governance strategies have worked in practice.

<div class="lab-area-pubs">
{% assign area_pubs = site.data.publications | where: "area", "law" | sort: "year" | reverse %}
{% for pub in area_pubs %}
  {% include publication-entry.html %}
{% endfor %}
</div>
</div>
</details>

<details class="lab-area" markdown="1">
<summary>Learning from and auditing AI deployments on the ground</summary>
<div class="lab-area-body" markdown="1">
We study how AI systems are actually used in practice and build methods to audit real deployments and their impacts. This work helps us understand what problems and harms are happening in the real world, which helps guide our technical and legal/governance research.

<div class="lab-area-pubs">
{% assign area_pubs = site.data.publications | where: "area", "deployments" | sort: "year" | reverse %}
{% for pub in area_pubs %}
  {% include publication-entry.html %}
{% endfor %}
</div>
</div>
</details>

## <a id="team"></a>Team


| ![Emily Black]({{ '/images/teampics/emily.jpg' | relative_url }}){: .team-headshot } | ![Falaah Arif Khan]({{ '/images/teampics/falaah.jpg' | relative_url }}){: .team-headshot } | ![Eliza Berman]({{ '/images/teampics/eliza.jpg' | relative_url }}){: .team-headshot } | ![Sajel Surati]({{ '/images/teampics/sajel.png' | relative_url }}){: .team-headshot } |
| **[Emily Black](https://emblack.github.io/)** | **[Falaah Arif Khan](https://falaaharifkhan.github.io/research/)** | **[Eliza Berman](https://elizaberman.github.io/)** | **[Sajel Surati](https://sajelsurati.com/)** |
| Principal Investigator | PhD Student | PhD Student | PhD Student |

| ![Qihan Wang]({{ '/images/teampics/qihan.jpg' | relative_url }}){: .team-headshot } | ![Bella Chang]({{ '/images/teampics/bella.jpeg' | relative_url }}){: .team-headshot } | ![Hoon Cho]({{ '/images/teampics/hoon.jpg' | relative_url }}){: .team-headshot } | ![Chuhan Ku]({{ '/images/teampics/chuhan.jpg' | relative_url }}){: .team-headshot } |
| **Qihan Wang** | **Bella Chang** | **Hoon Cho** | **Chuhan Ku** |
| M.S. Student | M.S. Student | M.S. Student | M.S. Student |

| ![Gordon Dai]({{ '/images/teampics/gordon.jpg' | relative_url }}){: .team-headshot } | ![Riley Stacy]({{ '/images/teampics/riley.jpg' | relative_url }}){: .team-headshot } |  |  |
| **Gordon Dai** | **Riley Stacy** |  |  |
| B.A. Student | B.S. Student (Barnard) |  |  |
{: .team-table }

## <a id="open-positions"></a>Open Positions

We are hiring a postdoc to develop technical evaluation methods for detecting discrimination and instability in generative AI systems used in hiring and credit decisions. This is a unique opportunity to develop methods with real-world impact, as we anticipate collaborating with industry partners in HR tech and fintech to ground our methods in real workflows. (Dates: September 2026 – August 2027, with potential to extend to two years).

We're looking for:
* PhD in Computer Science or related field (completed or expected before start).
* Strong background in generative AI and/or AI evaluation, with publications at venues such as FAccT, NeurIPS, ICML, ICLR, AAAI, ACL or similar.
* Background or interest in responsible AI / algorithmic fairness.

To apply, please send a CV, brief research statement (1pg), 2–3 representative papers, and names of 2-3 references to eb1850@nyu.edu with "Postdoc Application" in the subject. Applications reviewed on a rolling basis. Please feel free to reach out for more information.
