---
title: Accepted abstracts
layout: page
# feature_image: 
# image_source: 
---

{%- for paper in site.data.papers -%}
  <li>
    <span class="text-muted mr-2">{{ paper.authors | array_to_sentence_string }}</span> 
    {{ paper.title }}
  </li>    
{%- endfor -%}
