---
layout: default
wide: true
title: Open Data Resources
---

{% for resource in site.resources %}
{{ resource }}
<br /><br />
{% endfor %}

<div class="resources">
  {% include resources-landing.html %}
  <ul class="results">
    {% for page in site.pages %}
    {% if page.section == 'resources' %}
    {% include resources-results.html resource=page %}
    {% endif %}
    {% endfor %}
  </ul>
</div>