---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

You can find the list of my publications at [NASA ADS](https://ui.adsabs.harvard.edu/user/libraries/tbxiKajfTsSjDC7Ir7sZxA) and [Google Scholar](https://scholar.google.com/citations?user=nGVc2BAAAAAJ&hl=en). 

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
