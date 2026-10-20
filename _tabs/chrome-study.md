---
layout: page
title: Study
permalink: /target/browser/chrome/study/
---
{% include research-style.html %}
<div class="research-crumb"><a href="{{ '/target/' | relative_url }}">Target</a> / <a href="{{ '/target/browser/' | relative_url }}">Browser</a> / <a href="{{ '/target/browser/chrome/' | relative_url }}">Chrome</a> / Study</div>
<div class="research-kicker">KNOWLEDGE BASE</div>
<p class="research-intro">V8과 Chrome의 내부 구조, 소스 코드 분석, 검증 실험을 기록하는 공간입니다.</p>
<h2 class="research-section-title">Study Notes</h2>
{% assign count = 0 %}
{% for post in site.posts %}
{% if post.categories contains 'Browser' and post.categories contains 'Chrome' and post.tags contains 'study' %}
<a class="research-entry" href="{{ post.url | relative_url }}"><strong>{{ post.title | escape }}</strong><small>{{ post.date | date: '%Y-%m-%d' }}{% if post.description %} &middot; {{ post.description | escape }}{% endif %}</small></a>
{% assign count = count | plus: 1 %}
{% endif %}
{% endfor %}
{% if count == 0 %}<div class="research-empty"><i class="fas fa-book-open"></i><p>아직 게시된 Study 글이 없습니다.</p></div>{% endif %}
