---
title: Accepted abstracts
layout: page
# feature_image: 
# image_source: 
---

{%- for paper in site.data.papers -%}
  <li>
    <span class="text-muted mr-2">{{ paper.authors | array_to_sentence_string }}</span> 
    <a target="_blank" href="{{ "/papers/" | append: paper.extended_abstract | relative_url }}">{{ paper.title }}</a>
  </li>    
{%- endfor -%}
