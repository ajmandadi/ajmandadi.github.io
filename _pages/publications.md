---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

<style>
  .publications-list li { margin-bottom: 1em; }
</style>

<ol class="publications-list">
{% for post in site.publications reversed %}
  <li>{{ post.citation }}. <strong>"<i>{% if post.paperurl %}<a href="{{ post.paperurl }}">{{ post.title }}</a>{% else %}{{ post.title }}{% endif %}</i>"</strong>. {% if post.venue_prefix %}{{ post.venue_prefix }} {% endif %}{{ post.venue }}, {{ post.date | date: "%Y" }}.</li>
{% endfor %}
</ol>
