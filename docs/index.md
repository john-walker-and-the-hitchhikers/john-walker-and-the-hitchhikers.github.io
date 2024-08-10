---
title: Welcome
layout: home
---

{% assign sorted_pages = site.pages | sort:"order" %}
{%- for p in site.pages -%}
    {%- if p.album -%}
        {% include album-cover-with-links.html
            title=p.title
            album=p.album
            href=p.url
            message=p.message
            streaming=p.streaming  %}
    {%- endif -%}
{%- endfor -%}
