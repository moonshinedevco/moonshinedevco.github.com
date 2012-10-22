---
layout: base
title: "FindingScience : a blog about startup tech and gallimaufry"
---

{% for post in site.posts offset: 0 limit: 10 %}
# <a class="opbandit" href='{{ post.id }}.html'>{{ post.title }}</a>
<span id="date">Posted {{ post.date | date_to_string }}{% include tags.markdown %}and has <a href="{{ post.id }}.html#disqus_thread">Comments</a></span>
  {{ post.content }}
<span class="padding"></span>
{% endfor %}


<script type="text/javascript">
  _veroq.push(['track', 'visited_home_page']);
</script>