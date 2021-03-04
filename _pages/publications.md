---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

You can find my publications on <u><a href="{{ author.dblp }}">my dblp profile</a></u>.


{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
