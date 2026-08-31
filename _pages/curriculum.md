---
title: "The Reading Plan"
permalink: /curriculum/
excerpt: "Twelve weeks from early Buddhism to the many traditions that followed."
---

This is our first pass through a very large subject. We start with early Buddhism, spend time with a few core teachings and practices, then follow the history into the traditions that developed afterward.

The reading lists are still taking shape. We’re adding texts as we choose and check them, rather than filling twelve pages with impressive-looking links we have not read yet.

{% assign ordered_weeks = site.weeks | sort: "order" %}
{% for item in ordered_weeks %}
## [Week {{ item.week }}: {{ item.topic }}]({{ item.url | relative_url }})

{{ item.orientation }}
{% endfor %}
