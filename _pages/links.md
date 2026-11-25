---
layout: page
title: links
permalink: /links/
description: My CV, research and academic profiles in one place.
nav: true
nav_order: 1
# Resume: put your resume PDF in assets/pdf/ with this file name. Until then its card shows "Coming soon".
resume_pdf: danielUdekweResume.pdf
---

{% capture resume_path %}assets/pdf/{{ page.resume_pdf }}{% endcapture %}
{% capture resume_exists %}{% file_exists {{ resume_path }} %}{% endcapture %}

<h3 class="link-section-title">CV and resume</h3>
<div class="link-cards">
<a class="link-card" href="{{ '/assets/pdf/danielUdekweCV_A.pdf' | relative_url }}" target="_blank" rel="noopener">
<i class="fa-solid fa-file-pdf link-card-icon"></i>
<span class="link-card-text">
<span class="link-card-title">CV</span>
<span class="link-card-desc">Full academic CV (PDF)</span>
</span>
</a>
{% if resume_exists == "true" %}
<a class="link-card" href="{{ resume_path | prepend: '/' | relative_url }}" target="_blank" rel="noopener">
<i class="fa-solid fa-file-lines link-card-icon"></i>
<span class="link-card-text">
<span class="link-card-title">Resume</span>
<span class="link-card-desc">One-page resume (PDF)</span>
</span>
</a>
{% else %}
<div class="link-card link-card-disabled" title="Resume coming soon">
<i class="fa-solid fa-file-lines link-card-icon"></i>
<span class="link-card-text">
<span class="link-card-title">Resume</span>
<span class="link-card-desc">Coming soon</span>
</span>
</div>
{% endif %}
</div>

<h3 class="link-section-title">Research</h3>
<div class="link-cards">
<a class="link-card" href="{{ '/publications/' | relative_url }}">
<i class="fa-solid fa-book-open link-card-icon"></i>
<span class="link-card-text">
<span class="link-card-title">Publications</span>
<span class="link-card-desc">Journal articles and preprints</span>
</span>
</a>
<a class="link-card" href="{{ '/project/' | relative_url }}">
<i class="fa-solid fa-flask link-card-icon"></i>
<span class="link-card-text">
<span class="link-card-title">Projects</span>
<span class="link-card-desc">Research projects and demos</span>
</span>
</a>
<a class="link-card" href="{{ '/media/' | relative_url }}">
<i class="fa-solid fa-photo-film link-card-icon"></i>
<span class="link-card-text">
<span class="link-card-title">Media</span>
<span class="link-card-desc">Photos and highlights</span>
</span>
</a>
<a class="link-card" href="{{ '/repositories/' | relative_url }}">
<i class="fa-solid fa-code-branch link-card-icon"></i>
<span class="link-card-text">
<span class="link-card-title">Repositories</span>
<span class="link-card-desc">Code for my research</span>
</span>
</a>
</div>

<h3 class="link-section-title">Profiles</h3>
<div class="link-cards">
{% if site.scholar_userid %}
<a class="link-card" href="https://scholar.google.com/citations?user={{ site.scholar_userid }}" target="_blank" rel="noopener">
<i class="ai ai-google-scholar link-card-icon"></i>
<span class="link-card-text">
<span class="link-card-title">Google Scholar</span>
<span class="link-card-desc">Publications and citations</span>
</span>
</a>
{% endif %}
{% if site.linkedin_username %}
<a class="link-card" href="https://www.linkedin.com/in/{{ site.linkedin_username }}" target="_blank" rel="noopener">
<i class="fa-brands fa-linkedin link-card-icon"></i>
<span class="link-card-text">
<span class="link-card-title">LinkedIn</span>
<span class="link-card-desc">Professional profile</span>
</span>
</a>
{% endif %}
{% if site.github_username %}
<a class="link-card" href="https://github.com/{{ site.github_username }}" target="_blank" rel="noopener">
<i class="fa-brands fa-github link-card-icon"></i>
<span class="link-card-text">
<span class="link-card-title">GitHub</span>
<span class="link-card-desc">Code and research repositories</span>
</span>
</a>
{% endif %}
</div>
