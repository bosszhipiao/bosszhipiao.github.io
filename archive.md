---
layout: default
title: 时间长河
permalink: /archive/
---

<section class="container page-section">
  <h1>时间长河</h1>

  {% comment %}收集所有年份并去重排序{% endcomment %}
  {% capture years_str %}{% for post in site.posts %}{{ post.date | date: "%Y" }}|{% endfor %}{% endcapture %}
  {% assign all_years = years_str | split: "|" | uniq | sort | reverse %}

  {% for year in all_years %}
    {% if year == "" %}{% continue %}{% endif %}
  <div id="{{ year }}" class="archive-year">
    <h2>{{ year }}年</h2>
    <ul class="archive-list">
      {% assign year_posts = site.posts | sort: "date" | reverse %}
      {% for post in year_posts %}
        {% assign post_year = post.date | date: "%Y" %}
        {% if post_year == year %}
        <li>
          <span class="archive-date">{{ post.date | date: "%m月%d日" }}</span>
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          {% if post.categories %}
            <span style="color:var(--muted);font-size:0.82rem;">
              {% for cat in post.categories %}· {{ cat }} {% endfor %}
            </span>
          {% endif %}
        </li>
        {% endif %}
      {% endfor %}
    </ul>
  </div>
  {% endfor %}
</section>
