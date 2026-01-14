---
layout: default
title: "Archetype Core Notes"
---

# Archetype Core Notes

Short field memos on data systems, governance, security, and the decisions that make systems trustworthy.

## Issues
<ul>
  {% assign sorted = site.issues | sort: "date" | reverse %}
  {% for issue in sorted %}
    <li>
      <a href="{{ issue.url }}">{{ issue.title }}</a>
      <span style="opacity:0.7;">({{ issue.date | date: "%b %d, %Y" }})</span>
    </li>
  {% endfor %}
</ul>
