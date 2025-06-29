---
layout: page
title: الأدوات
permalink: /tools/
---

## جميع أدواتنا

{% for tool in site.data.navigation.main[2].dropdown %}
  - [{{ tool.name }}]({{ tool.url }})
{% endfor %}
