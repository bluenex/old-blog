---
layout: default
title: Tags Archive
comment: false
permalink: /tags/
---
<style>
.tags {
  display: block;
  font-size: 1.25rem;
  /*font-weight: bold;*/
  color: #4183C4;
  list-style: none;
  margin-left: 0;
  padding-left: 0;
}

.tags li {
  display: inline;
}

.tags li a {
  margin-top: 0;
}

.tag {
  line-height: 1.4;
  display: inline-block;
  background-color: #FFF;

  padding: 0px 11px;
  margin: 10px 3px 0 0;
  border-radius: 2px;
  border: solid 1px #EEE;
}

.tag .count {
  color: red;
  font-weight: bold;
}
</style>

<article>
  {% capture site_tags %}{% for tag in site.tags %}{{ tag | first }}{% unless forloop.last %},{% endunless %}{% endfor %}{% endcapture %}
  {% assign tags_list = site_tags | split:',' | sort %}

  <ul class="tags">
    {% for item in (0..site.tags.size) %}{% unless forloop.last %}
      {% capture this_word %}{{ tags_list[item] | strip_newlines }}{% endcapture %}
      <li><a href="#{{ this_word }}" class="tag"><span class="term">{{ this_word }}</span>&nbsp;&nbsp;<span class="count">{{ site.tags[this_word].size }}</span></a></li>
    {% endunless %}{% endfor %}
  </ul>

  {% for item in (0..site.tags.size) %}{% unless forloop.last %}
  {% capture this_word %}{{ tags_list[item] | strip_newlines }}{% endcapture %}
	<article>
	<h2 id="{{ this_word }}" class="tag-heading">{{ this_word }}</h2>
		<ul>
    {% for post in site.tags[this_word] %}{% if post.title != null %}
      <li><a href="{{ site.url }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a></li>
    {% endif %}{% endfor %}
		</ul>
	</article><!-- /.hentry -->
{% endunless %}{% endfor %}
</article>
