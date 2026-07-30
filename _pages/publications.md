---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: false
---

{% if site.author.googlescholar %}
<p class="pub-scholar-link">You can also find my papers on <a href="{{ site.author.googlescholar }}">my Google Scholar profile</a>.</p>
{% endif %}

{% comment %}
  Newest first. Years are walked in descending order and entries are emitted in
  _data/publications.yml order within each year, so papers sharing a year keep the
  ordering set in the data file rather than an arbitrary sort order.
{% endcomment %}
{% assign years = site.data.publications | map: "year" | uniq | sort | reverse %}
{% for year in years %}
  {% for pub in site.data.publications %}
    {% if pub.year != year %}{% continue %}{% endif %}
    {% include publication-entry.html %}
  {% endfor %}
{% endfor %}

{% include publication-lightbox.html %}
