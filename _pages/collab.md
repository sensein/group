---
title: "The Group - Collaborators"
layout: gridlay
excerpt: "The Group: Collaborators"
sitemap: false
permalink: /collab/
---

## Our collaboration policies are:

- Authorship is a function of intellectual contribution and we try to minimize 
author bloat in our group. For multi-institution student collaborations, we will 
identify ahead of time who the primary advisers and collaborators are on a 
project.
- Our work is open. However, there have been prior situations where we have 
applied for patents during collaborations.
- We tend to share any data we collect and any code we produce under open 
licenses (data: PDDL, code: Apache 2.0, doc: CC-BY)
- Any digital research work we produce together should be re-executable and hopefully 
reproducible/generalizable.

# Collaborators

<em>** This list may not always be accurate. We apologize if we missed your name, 
listed incorrect information or did not ask you before listing you. Please let us 
know so we can rectify the situation.</em>

{% for site in site.data.collaborators %}

{% for person in site.persons %}

  <em>{{ person.name }} </em>, {{ site.home }}<br />

{% endfor %}
{% endfor %}
