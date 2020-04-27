---
title: "Research"
layout: textlay
excerpt: "Research"
sitemap: false
permalink: /research/
---

# Research

<img src="{{ "/images/multi_sensory_integration.png" | prepend: site.baseurl | prepend: site.url}}" class="img-responsive" width="50%" style="float: right; margin: 0.8%; min-width: 350px" />

A fundamental problem in psychiatry is that there are no biological markers for 
diagnosing mental illness or for indicating how best to treat it. Treatment 
decisions are based entirely on symptoms, and doctors and their patients will 
typically try one treatment, then if it does not work, try another, and perhaps 
another. Our group hopes to change this picture, and our research suggests 
that individual brain scans and speaking patterns can hold valuable information 
for guiding psychiatrists and patients. Current areas include depression, 
suicide, anxiety disorders, autism, Parkinson disease, and brain tumors.

To support this broader goal, our group develops novel analytic platforms that 
use such information to create robust, predictive models around human health. We 
believe that solving this problem will require complex integration of different
types of sensors into an adaptive learning system together with patient, caregiver,
and community feedback.

Our research interests span computer science and neuroscience, specifically in 
the areas of applied machine learning, signal processing, and translational 
medicine. Our current research portfolio comprises projects on spoken 
communication, brain imaging, and informatics to address gaps in scientific 
knowledge in three areas: the neural basis and translational applications of 
speaking, precision psychiatry and medicine, and preserving information for 
reproducible research.

Many of the tools we develop can be used across domains. If you have a 
need we can address, we would like to hear from you.

If you have solved problems associated with any of the projects below, we would 
love to hear from you. For us, a solution typically implies available data, 
code, and/or replicated results.
 
## Highlights

For a full list see [below](#full-list)

{% assign number_printed = 0 %}
{% for proj in site.data.projects %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if proj.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ proj.title }}</pubtit>
  <img src="{{ proj.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ proj.description }}</p>
  <p><em>{{ proj.authors }}</em></p>
  <p><strong><a href="{{ proj.link.url }}">{{ proj.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ proj.news1 }}</strong></p>
  <p> {{ proj.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>


## Full List

{% for proj in site.data.projects %}

  <b>{{ proj.title }}</b> <br />
  <em>{{ proj.authors }} </em><br />
  {{ proj.description }}<br />
  <a href="{{ proj.link.url }}">{{ proj.link.display }}</a>

{% endfor %}

