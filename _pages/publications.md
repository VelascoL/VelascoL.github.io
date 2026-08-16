---
layout: default
title: "Publications"
---

<h1>Publications and Preprints</h1>

<ul>
  {% assign pubs = site.projects | sort: "year" | reverse %}

{% for pub in pubs %}

* {{ pub.title }}  
  {{ pub.authors }}  
  {{ pub.journal }}, {{ pub.year }}.
  {% if pub.note %} {{ pub.note }} {% endif %}  
  {% if pub.arxivlink %}<a href="{{ pub.arxivlink }}" target="_blank">arXiv</a>{% endif %}
  {% if pub.arxivlink and pub.journallink %} | {% endif %}
  {% if pub.journallink %}<a href="{{ pub.journallink }}" target="_blank">Journal</a>{% endif %}

{% endfor %}
</ul>
