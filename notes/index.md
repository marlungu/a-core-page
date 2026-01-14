---
title: "Notes"
permalink: /notes/
---

Short field memos on data systems, governance, security, and the decisions that make systems trustworthy.

## Issues

<ul class="issues-list">
{% assign sorted = site.issues | sort: "date" | reverse %}
{% for issue in sorted %}
  <li class="issue-row">
    <a href="{{ issue.url }}">{{ issue.title }}</a>
    <span class="issue-date">{{ issue.date | date: "%b %d, %Y" }}</span>
  </li>
{% endfor %}
</ul>
