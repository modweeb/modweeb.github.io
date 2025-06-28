---
layout: tags
icon: fas fa-tags
order: 3
title: الوسوم
---

<blockquote class="tags-intro">
🏷️ نظام الوسوم المتقدم في مود ويب  
تصفح المقالات عبر وسوم دقيقة مثل #يمن_نت #بلوجر #SEO #أدوات_مجانية
</blockquote>

<div class="notice--success" markdown="1">
✨ **ميزة جديدة:** انقر على أي وسم لمشاهدة جميع المقالات المرتبطة به!
</div>

<div class="tags-cloud" style="text-align: center; margin: 1.5em 0;">
{% assign sorted_tags = site.tags | sort %}
{% for tag in sorted_tags %}
  {% assign tag_size = tag[1].size %}
  <a href="{{ site.baseurl }}/tags/{{ tag[0] | slugify }}" 
     class="tag-link"
     style="font-size: {{ tag_size | times: 2 | plus: 12 }}px;">
    #{{ tag[0] }}
  </a>
{% endfor %}
</div>

<style>
.tag-link {
  margin: 0 0.3em;
  line-height: 2;
  display: inline-block;
  transition: all 0.3s ease;
}
.tag-link:hover {
  transform: scale(1.1);
  color: var(--link-hover-color);
}
</style>
