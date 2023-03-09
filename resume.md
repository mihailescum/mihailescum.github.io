---
layout: default
permalink: "/resume"
title: Max Mihailescu - Resume

cv_pdf: "#"
---
<br />
You can find a full CV [here]({{ page.cv_pdf | relative_url }}).

<section id="sec-education">
<h3 class="cv-section-header">Education</h3>

{% for item in site.data.resume.education %}
<div class="cv-entry">
    <h4 class="cv-entry-title">{{ item.title }} <small> | {{ item.place }} &bull; {{ item.period }}</small></h4>
    {% if item.description %}<p class="cv-entry-description">{{ item.description }}</p>{% endif %}
</div>
{% endfor %}

<section id="sec-education">
<h3 class="cv-section-header">Work Experience</h3>

{% for item in site.data.resume.work %}
<div class="cv-entry">
    <h4 class="cv-entry-title">{{ item.title }} <small> | {{ item.place }} &bull; {{ item.period }}</small></h4>
    {% if item.description %}<p class="cv-entry-description">{{ item.description }}</p>{% endif %}
</div>
{% endfor %}
</section>
