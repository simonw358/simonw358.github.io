---
layout: single
title: "CV & Publications"
permalink: /cv_publications/
author_profile: true
redirect_from:
  - /cv_publications.html
---

<style>
  .cv-links {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin: 0 0 1.5rem;
    padding: 0;
    list-style: none;
  }

  .cv-frame {
    width: 100%;
    min-height: 800px;
    border: 1px solid #d8d8d8;
    border-radius: 4px;
    margin-bottom: 1rem;
  }

  @media (max-width: 736px) {
    .cv-frame {
      min-height: 560px;
    }
  }
</style>

For the most up-to-date publication lists, please see my external profiles:

{% if site.github.build_revision %}
  {% assign cv_version = site.github.build_revision %}
{% else %}
  {% assign cv_version = site.time | date: "%s" %}
{% endif %}

<ul class="cv-links">
  <li><a href="{{ site.author.ads }}" class="btn" target="_blank" rel="noopener">NASA ADS</a></li>
  <li><a href="{{ site.author.googlescholar }}" class="btn" target="_blank" rel="noopener">Google Scholar</a></li>
  <li><a href="{{ site.author.orcid }}" class="btn" target="_blank" rel="noopener">ORCID</a></li>
  <li><a href="{{ base_path }}/files/Simon_Weng_CV.pdf?v={{ cv_version }}" class="btn" download>Download CV</a></li>
</ul>

<iframe class="cv-frame" src="{{ base_path }}/files/Simon_Weng_CV.pdf?v={{ cv_version }}#page=1&view=FitH&navpanes=0" title="Simon Weng CV"></iframe>
