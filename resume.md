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

{% for item in site.data.resume.education %}
<div class="cv-entry">
    <h3 class="cv-entry-title">{{ item.title }} <small> | {{ item.place }} &bull; {{ item.period }}</small></h3>
    {% if item.description %}<p class="cv-entry-description">{{ item.description }}</p>{% endif %}
</div>
{% endfor %}

<section id="sec-education">
<h2 class="cv-section-header">Work Experience</h2>

{% for item in site.data.resume.work %}
<div class="cv-entry">
    <h3 class="cv-entry-title">{{ item.title }} <small> | {{ item.place }} &bull; {{ item.period }}</small></h3>
    {% if item.description %}<p class="cv-entry-description">{{ item.description }}</p>{% endif %}
</div>
{% endfor %}
</section>
