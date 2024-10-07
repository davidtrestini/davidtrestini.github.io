---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

A PDF version of my publication list can be found below:
<center><a href="../files/publication_list.pdf" download="David_Trestini_publications.pdf"><button class="btn btn--custom">Publication list</button></a></center>

You can also find my papers on  <a href="https://inspirehep.net/authors/2018015" target="_blank" rel="noopener"><i class="ai ai-inspire ai-fw"></i> iNSPIRE</a>, <a href="https://ui.adsabs.harvard.edu/search/fq=%7B!type%3Daqp%20v%3D%24fq_database%7D&fq_database=(database%3Aastronomy%20OR%20database%3Aphysics)&q=%20author%3A%22trestini%2C%20david%22&sort=date%20desc%2C%20bibcode%20desc&p_=0" target="_blank" rel="noopener"><i class="ai ai-ads-square ai-fw"></i> NASA/ADS</a>, <a href="{{site.author.googlescholar}}" target="_blank" rel="noopener"><i class="ai ai-google-scholar-square ai-fw"></i> Scholar</a> or the <a href="https://arxiv.org/a/trestini_d_1.html" target="_blank" rel="noopener"><i class="ai ai-arxiv ai-fw"></i> arXiv</a>.



{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

<!-- New style rendering if publication categories are defined -->
{% if site.publication_category %}
  {% for category in site.publication_category  %}
    {% assign title_shown = false %}
    {% for post in site.publications reversed %}
      {% if post.category != category[0] %}
        {% continue %}
      {% endif %}
      {% unless title_shown %}
        <h2>{{ category[1].title }}</h2><hr />
        {% assign title_shown = true %}
      {% endunless %}
      {% include archive-single.html %}
    {% endfor %}
  {% endfor %}
{% else %}
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}



