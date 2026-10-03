---
layout: archive
title: "People"
permalink: /people/
author_profile: true
---

## People

{% for person in site.data.people %}
<div class="lab-member">
<h3 id="{{ person.name | slugify }}">{{ person.name }}</h3>
{% if person.photo %}<img src="{{ person.photo | relative_url }}" alt="Photo of {{ person.name }}" class="lab-member__photo">{% endif %}
<p><strong>{{ person.role }}</strong><br>{{ person.topic }}</p>
<p class="lab-member__links">
{% if person.website %}<a href="{{ person.website }}"><i class="fas fa-fw fa-link" aria-hidden="true"></i> Website</a>{% endif %}
{% if person.github %}<a href="https://github.com/{{ person.github }}"><i class="fab fa-fw fa-github" aria-hidden="true"></i> GitHub</a>{% endif %}
{% if person.scholar %}<a href="{{ person.scholar }}"><i class="ai ai-fw ai-google-scholar" aria-hidden="true"></i> Google Scholar</a>{% endif %}
</p>
</div>
{% endfor %}

## Alumni

<ul class="lab-list">
{% for person in site.data.alumni %}
<li>{% if person.website %}<a href="{{ person.website }}">{{ person.name }}</a>{% else %}{{ person.name }}{% endif %}{% if person.role %}, {{ person.role }}{% endif %}{% if person.years %} ({{ person.years }}){% endif %}{% if person.now %}. Now: {{ person.now }}{% endif %}</li>
{% endfor %}
</ul>
