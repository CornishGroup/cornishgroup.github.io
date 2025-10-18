---
title: "News Archive"
layout: textlay
excerpt: "Cornish Labs at Durham University."
sitemap: false
permalink: /news.html
---

# News

{% for article in site.data.news %}
<p>{{ **article.date** }} <br> {{ article.headline | markdownify | remove: '<p>' | remove: '</p>' }}</p>
{% endfor %}
