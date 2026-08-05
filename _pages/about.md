---
permalink: /
title: "About Me"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

?? Greetings! I am Zhishao Ni, a master?s student at East China Jiaotong University under the supervision of Professor Dequan Zeng.

?? My current research interests include reinforcement learning for autonomous vehicles.

I am currently seeking PhD opportunities and would welcome opportunities to conduct research in safe autonomous driving and end-to-end driving systems.

## Contact

Please feel free to contact me by email for academic communication and collaboration.

## Publications

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my publications on <a href="{{ site.author.googlescholar }}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

{% if site.publication_category %}
  {% for category in site.publication_category %}
    {% assign title_shown = false %}
    {% for post in site.publications reversed %}
      {% if post.category != category[0] %}
        {% continue %}
      {% endif %}
      {% unless title_shown %}
        <h3>{{ category[1].title }}</h3>
        <hr />
        {% assign title_shown = true %}
      {% endunless %}
      {% include archive-single.html %}
    {% endfor %}
  {% endfor %}
{% else %}
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}