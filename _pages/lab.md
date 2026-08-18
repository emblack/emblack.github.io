---
layout: archive
title: "IDEA Lab"
permalink: /lab/
author_profile: false
---

<img
  src="{{ '/images/logo.png' | relative_url }}"
  alt="IDEA LAB logo"
  style="width:500px; max-width:95%; height:auto; display:block; margin: 6px auto 10px auto;"
/>
We are the **IDEA (Impact-Driven Evaluation for AI) Lab** in **NYU Computer Science**, led by Dr. Emily Black. Our research develops methods to measure and mitigate harm from AI systems, with a special focus on preventing harm in the real world.

<div class="pub-area-nav">
  <a href="#research">Research</a>
  <a href="#team">Team</a>
  <a href="#working-together">Working Together</a>
  <a href="#alumni">Lab Alumni</a>
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

<div class="team-grid">
{% assign current_members = site.data.team | where_exp: "member", "member.alumni != true" %}
{% for member in current_members %}
  {% include team-member.html %}
{% endfor %}
</div>

## <a id="working-together"></a>Working Together

**PhD applicants:** Please apply to the NYU PhD program and list me as a faculty member of interest on your application.

**Masters students:** I generally do not take on masters students who have not taken one of my classes. If you have taken my class and are interested in working with me, please reach out.

{% assign alumni = site.data.team | where_exp: "member", "member.alumni == true" %}
{% if alumni.size > 0 %}
## <a id="alumni"></a>Lab Alumni

<ul class="alumni-list">
{% for member in alumni %}
  <li>
    <span class="alumni-name">{% if member.url %}<a href="{{ member.url }}">{{ member.name }}</a>{% else %}{{ member.name }}{% endif %}</span>
    <span class="alumni-role">{{ member.role }}</span>
  </li>
{% endfor %}
</ul>
{% endif %}

{% include publication-lightbox.html %}
