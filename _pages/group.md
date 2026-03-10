---
layout: page
title: group
permalink: /group/
description: Members of our research group.
nav: true
nav_order: 7
---

## Group Members

{% for category in site.data.group_members %}
### {{ category.title }}

{% for member in category.members %}
- {% if member.website %}<a href="{{ member.website }}" target="_blank">{{ member.name }}</a>{% else %}{{ member.name }}{% endif %}{% if member.note %} ({{ member.note }}){% endif %}
{% endfor %}

{% endfor %}
