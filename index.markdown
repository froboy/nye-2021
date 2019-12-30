---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
---

{% for course in site.data.courses offset:6 %}
{% if course.What %}
<div class="dish">
    <h4 class="text-muted">{{ course.Course }}</h4>
    <h2>{{ course.What }}</h2>
    <h3 class="text-muted">by {{ course.Who }}</h3>
    <p>{{ course.Recipe }}</p>
    {% if course.Pairing %}
    <p>Served with: {{ course.Pairing }}</p>
    {% endif %}
    <p><small>Contains:</small></p>
</div>
{% endif %}
{% endfor %}