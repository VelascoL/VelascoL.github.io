---
layout: default
title: "Publications"
---

<h1>Publications</h1>

<ul>
  {% assign pubs = site.projects| sort: "year" | reverse %}
  {% for pub in pubs %}
    <li>
      <strong>{{ pub.title }}</strong><br>
      {{ pub.authors }}<br>
      <em>{{ pub.journal }}</em>, {{ pub.year }}.<br>
      {% if pub.note %}
        <span style="color: gray;">{{ pub.note }}</span>
      {% endif %}<br>
      {% if pub.link %}
        <a href="{{ pub.link }}" target="_blank">[link]</a>
      {% endif %}
    </li>
  {% endfor %}
</ul>
