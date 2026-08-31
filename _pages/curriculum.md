---
title: "Twelve-Week Curriculum"
permalink: /curriculum/
excerpt: "A first pass through Buddhist history, early teachings, and the development of major traditions."
sidebar:
  nav: "curriculum"
---

This course begins with the historical and religious world in which Buddhism emerged, then reads across early teachings and practices before tracing the development of major Buddhist traditions.

The weekly pages are structured outlines. Specific primary and secondary readings will be added only after they have been checked for accuracy, context, translation quality, and stable public access.
{: .notice--info}

{% assign ordered_weeks = site.weeks | sort: "order" %}
{% for item in ordered_weeks %}
## [Week {{ item.week }}: {{ item.topic }}]({{ item.url | relative_url }})

{{ item.orientation }}
{% endfor %}
