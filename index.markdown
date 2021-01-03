---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
---

<p>Our December 31, 2020 party was held in traditional 2020 fashion—virtually. <a href="https://photos.app.goo.gl/ejqt2hTH6RxftwBi9">Check out the pics.</a></p>

<h2 class="post-list-heading">The Menu</h2>
<ul class="post-list">
    {% for course in site.data.courses offset:7 %}
    {% if course.What %}
    <li>
        <span class="post-meta">{{ course.Number }}: {{ course.Course }}</span>
        {% if course.Recipe %}
        <h3><a href="{{- course.Recipe -}}">{{- course.What -}}</a></h3>
        {% else %}
        <h3>{{ course.What }}</h3>
        {% endif %}
        <span class="post-meta">by {{ course.Who }}</span>
        <p>{{ course.Description }}</p>
        {% if course.Pairing %}
        <p>Served with: {{ course.Pairing }}</p>
        {% endif %}
        {% if course.Allergens %}
        <p><small>Contains: {{ course.Allergens }}</small></p>
        {% endif %}
    </li>
    {% endif %}
    {% endfor %}
</ul>
