---
layout: home
title: Home
nav_order: 0
description: >-
    Just the Class is a modern, highly customizable, responsive Jekyll theme
    for developing course websites.
---

# {{ site.description }}
{: .mb-2 }
{{ site.title }}
{: .fs-6 .text-grey-dk-000 }

{% if site.announcements %}
{{ site.announcements.last }}
[Announcements]({{ site.baseurl }}{% link announcements.md %}){: .btn .btn-outline .fs-3 }
{% for module in site.modules %}
{% if site.announcements.last.week == module.week %}{{ module }}{% endif %}
{% endfor %}
{% endif %}

---

## Calendar

{% for module in site.modules %}
{{ module }}
{% endfor %}
