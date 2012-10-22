---
layout: base
title: "Moonshine Dev. Co. Web Log"
---

{% for post in site.posts offset: 0 limit: 10 %}
# <a href='{{ post.id }}.html'>{{ post.title }}</a>
<span id="date">Posted {{ post.date | date_to_string }}{% include tags.markdown %}and has <a href="{{ post.id }}.html#disqus_thread">Comments</a></span>
  {{ post.content }}
<span class="padding"></span>
{% endfor %}
