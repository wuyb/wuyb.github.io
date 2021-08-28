---
layout: ten
title: 十年之前
permalink: /ten/
---

<div class="home">

  {%- if site.posts.size > 0 -%}
    <ul class="post-list">
      {%- for post in site.posts -%}
      {% capture year %}{{post.date | date: "%Y"}}{% endcapture %}
      {% if year < "2021" %}
      <li>
        {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
        <span class="post-meta">{{ post.date | date: date_format }}</span>
        <h3>
          <a class="post-link" href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
          </a>
        </h3>
        {%- if site.show_excerpts -%}
          {{ post.excerpt }}
        {%- endif -%}
      </li>
      {% endif %}
      {%- endfor -%}
    </ul>

  {%- endif -%}

</div>

