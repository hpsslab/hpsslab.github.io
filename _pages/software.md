---
title: "hpsslab Lab - Software"
layout: textlay
excerpt: "hpsslab Lab -- Software"
sitemap: false
permalink: /software/
---

# Software

## Publication Implementations

{% for item in site.data.software %}
{% if item.section == "publications" %}
**<a href="{{ item.link }}">{{ item.title }}</a>** — {{ item.description }}

{% endif %}
{% endfor %}

## Tools

{% for item in site.data.software %}
{% if item.section == "tools" %}
**<a href="{{ item.link }}">{{ item.title }}</a>** — {{ item.description }}

{% endif %}
{% endfor %}

## Software We Use

{% assign software_we_use = site.data.software | where: "section", "software_we_use" %}
{% assign categories = software_we_use | map: "category" | uniq %}
{% for cat in categories %}
### {{ cat }}

{% for item in software_we_use %}
{% if item.category == cat %}
**<a href="{{ item.link }}">{{ item.title }}</a>** — {{ item.description }}

{% endif %}
{% endfor %}
{% endfor %}
