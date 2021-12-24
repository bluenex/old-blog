---
layout: default
title: Tags Archive
comment: false
permalink: /tags/
---

<article id="tags">
  {% capture site_tags %}{% for tag in site.tags %}{{ tag | first }}{% unless forloop.last %},{% endunless %}{% endfor %}{% endcapture %}
  {% assign tags_list = site_tags | split:',' | sort %}

  <ul class="tags-container">
    {% for item in (0..site.tags.size) %}{% unless forloop.last %}
      {% capture this_word %}{{ tags_list[item] | strip_newlines }}{% endcapture %}
      <li class="tag-item-container">
        <a href="#{{ this_word }}" class="tag-link">{{ this_word }}&nbsp;•&nbsp;<span class="count">{{ site.tags[this_word].size }}</span></a>
      </li>
    {% endunless %}{% endfor %}
  </ul>

  {% for item in (0..site.tags.size) %}{% unless forloop.last %}
  {% capture this_word %}{{ tags_list[item] | strip_newlines }}{% endcapture %}

  <article>
    <h3 id="{{ this_word }}" class="tag-heading">{{ this_word }}</h3>
    <ul>
    {% for post in site.tags[this_word] %}{% if post.title != null %}
      <li><a href="{{ site.url }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a></li>
    {% endif %}{% endfor %}
    </ul>
  </article><!-- /.hentry -->
{% endunless %}{% endfor %}
</article>
