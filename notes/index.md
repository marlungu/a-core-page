---
layout: notes
title: "Notes"
---

# Notes

<p class="notes-subtitle">Short field memos on data systems, governance, security, and the decisions that make systems trustworthy.</p>

<hr class="notes-divider" />

## Issues

<ul class="issue-list">
  {% assign sorted = site.issues | sort: "date" | reverse %}
  {% for issue in sorted %}
    <li>
      <a class="issue-card" href="{{ issue.url }}">
        <div class="issue-num">Issue {{ issue.name | replace: "issue-", "" }}</div>
        <div>
          <div class="issue-title">{{ issue.title }}</div>
          <div class="issue-sub">{{ issue.date | date: "%b %d, %Y" }}</div>
        </div>
      </a>
    </li>
  {% endfor %}
</ul>
