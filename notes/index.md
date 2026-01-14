---
layout: notes
title: "Notes"
---

<div class="notes-wrap">
  <div class="notes-kicker">Archetype Core · Notes</div>
  <h1 class="notes-title">Notes</h1>
  <p class="notes-subtitle">Short field memos on data systems, governance, security, and the decisions that make systems trustworthy.</p>

  <hr class="notes-divider" />

  <div class="notes-content">
    <h2>Issues</h2>

    <ul class="issue-list">
      {% assign sorted = site.issues | sort: "date" | reverse %}
      {% for issue in sorted %}
        <li style="margin-bottom:12px;">
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
  </div>
</div>
