---
layout: base
title: categories
---
{% for cat in site.categories | sort %}
{% capture tag %}{{ cat | first }}{% endcapture %}
<a name="{{ tag }}">
</a>
## {{ tag | replace:'_',' ' }}
<div class="postitemlist">
<ul>
{% for post in site.categories[tag] %}
{% include postitem.markdown %}
{% endfor %}
</ul>
</div>
{% endfor %}

