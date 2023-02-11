---
layout: page
title: 论语学录
permalink: /lunyu/
description: 论语之学，录以文字，以求方家雅正，更为三省吾身。
nav: false
nav_order: 13
display_sections: [学而篇, 为政篇, 八佾篇, 里仁篇, 公冶长篇, 雍也篇, 述而篇, 泰伯篇, 子罕篇, 乡党篇, 先进篇, 颜渊篇, 子路篇, 宪问篇, 卫灵公篇, 季氏篇, 阳货篇, 微子篇, 子张篇, 尧曰篇]
---



<!-- pages/lunyu.md -->
<div class="lunyu">

  <!-- Display categorized lunyu -->
  {%- for section in page.display_sections %}
    <div class="card mt-3 p-3">
      <h5 class="card-title font-weight-medium">{{ section }}</h5>
      {%- assign sectionized_lunyu = site.lunyu | where: "section", section -%}
      {%- assign sorted_lunyu = sectionized_lunyu | sort: "section_no" %}
      <div class="post card-text font-weight-light list-group list-group-flush">
        {%- for section in sorted_lunyu -%}
          <h6 class="ml-1 ml-md-4" style="font-size: 0.95rem;"><b>{{ section.section_no }}.</b> <a class="post-link" href="{{ section.url | relative_url }}"><span class="subitem"> {{ section.title }}</span></a></h6>
          {%- endfor %}
      </div>  
    </div>
  {% endfor %}

</div>
