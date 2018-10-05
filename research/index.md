---
layout: default
title: Research
navigation_weight: 2
---

## {{ page.title }}

### Papers/Preprints

{% assign papers = site.data.papers | sort: 'date' | reverse %}
{% for paper in papers %}
<div class="papers">
**{{ paper.title }}**{% if paper.with %} (with {{ paper.with }}){% endif %}{% if paper.comment %}<br/> {{ paper.comment }}.{% endif %}

{% for link in paper.links %} [\[{{ link[0] }}\]]({{ link[1] }}) {% endfor %}
</div>
{% endfor %}

### Code

<div class="papers">
{% for thing in site.data.code %}
**{{ thing.title }}**{% if thing.with %} (with {{ thing.with }}){% endif %}{% if thing.comment %}<br/> {{ thing.comment }}{% endif %}

{% for link in thing.links %} [\[{{ link[0] }}\]]({{ link[1] }}) {% endfor %}
</div>
{% endfor %}
