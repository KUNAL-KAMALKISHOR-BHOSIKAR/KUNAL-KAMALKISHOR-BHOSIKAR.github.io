---
layout: single
title: "Publications"
permalink: /publications/
author_profile: true
author: kunal
---

{% assign pubs = site.publications | sort: "year" | reverse %}

{% if pubs.size == 0 %}
**DEBUG:** No publications detected.
{% endif %}

## Conference Papers

{% for pub in pubs %}
- **{{ pub.title }}**  
  {{ pub.venue }}, {{ pub.year }}  
  {% if pub.paperurl %}[Paper]({{ pub.paperurl }}){% endif %}
{% endfor %}
