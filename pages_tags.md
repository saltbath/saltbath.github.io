---
layout: page
title: tags
url: /tag/
---


{% assign tags = site.tags | sort %}
{% for tag in tags %}
<h2>
 <span class="site-tag">
    <a href="/tag/{{ tag | first | slugify }}.html"
        style="font-size: {{ tag | last | size  |  times: 4 | plus: 80  }}%">
            {{ tag[0] | replace:'-', ' ' }} ({{ tag | last | size }})
    </a>
</span>
</h2>
{% endfor %}
