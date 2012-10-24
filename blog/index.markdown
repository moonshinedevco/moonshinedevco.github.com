---
layout: base
title: "Moonshine Dev. Co. Web Log"
---
{% for post in site.posts offset: 0 limit: 10 %}
<div class="post">
<h2><a href='{{ post.id }}.html'>{{ post.title }}</a></h2>
<div class="date">Posted {{ post.date | date_to_string }}{% include tags.markdown %}and has <a href="{{ post.id }}.html#disqus_thread">Comments</a></div>
{{ post.content }}
<span class="knot"></span>
</div>
{% endfor %}
