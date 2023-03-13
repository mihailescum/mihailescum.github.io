---
layout: default
permalink: "/resume"
title: Max Mihailescu - Resume

cv_pdf: "javascript:;"
---

<br />
You can find a full CV as PDF [here]({{ page.cv_pdf | relative_url }}).

<hr />

<section id="sec-education">
<h2 class="cv-section-header">Education</h2>

{% for item in site.resume reversed %}
{%- if item.type == "education" -%}
<div class="cv-entry">
    <h3 class="cv-entry-title">{{ item.title }} <small> | {{ item.place }} &bull; {% include cv_date_formatter.md date=item.start %} &mdash; {% if item.end %}{% include cv_date_formatter.md date=item.end %}{% else %}present{% endif %}</small></h3>
    {% if item.content %}<p class="cv-entry-description">{{ item.content | markdownify }}</p>{% endif %}
</div>
{%- endif -%}
{% endfor %}

<section id="sec-education">
<h2 class="cv-section-header">Work Experience</h2>

{% for item in site.resume reversed %}
{%- if item.type == "work" -%}
<div class="cv-entry">
    <h3 class="cv-entry-title">{{ item.title }} <small> | {{ item.place }} &bull; {% include cv_date_formatter.md date=item.start %} &mdash; {% if item.end %}{% include cv_date_formatter.md date=item.end %}{% else %}present{% endif %}</small></h3>
    {% if item.content %}<p class="cv-entry-description">{{ item.content | markdownify }}</p>{% endif %}
</div>
{%- endif -%}
{% endfor %}
</section>
