---
layout: default
title: "Publications and Preprints"
---

<h1>Publications and Preprints</h1>

{% assign pubs = site.projects | sort: "year" | reverse %}

<ul>
{% for pub in pubs %}
  <li>
    {{ pub.title }}<br>
    {{ pub.authors }}<br>

    {% if pub.journal %}
      {{ pub.journal }}, {{ pub.year }}.
    {% else %}
      Preprint, {{ pub.year }}.
    {% endif %}

    {% if pub.note %} {{ pub.note }} {% endif %}

    <br>

    {% if pub.arxivlink %}
      <a href="{{ pub.arxivlink }}" target="_blank">arXiv</a>
    {% endif %}

    {% if pub.arxivlink and pub.journallink %}
      |
    {% endif %}

    {% if pub.journallink %}
      <a href="{{ pub.journallink }}" target="_blank">Journal</a>
    {% endif %}
  </li>
{% endfor %}
</ul>
