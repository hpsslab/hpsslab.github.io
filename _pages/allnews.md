---
title: "News"
layout: textlay
excerpt: "𝕙𝘆𝕡𝗲𝕤𝘆𝕤 Lab at Colorado School of Mines."
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
{{ article.date }} <br>
{{ article.headline | markdownify}}
{% endfor %}
