---
layout: page
title: Contact
permalink: /contact/
description:
nav: true
nav_order: 2
---

<div class="contact-page">
<p class="contact-lead">{{ site.contact_note }}</p>
<div class="link-cards">
<a class="link-card" href="mailto:{{ site.email | encode_email }}">
<i class="fa-solid fa-envelope link-card-icon"></i>
<span class="link-card-text">
<span class="link-card-title">Email</span>
<span class="link-card-desc">{{ site.email }}</span>
</span>
</a>
<a class="link-card" href="https://www.google.com/maps/search/?api=1&query=1753+W+Paul+Dirac+Dr+Tallahassee+FL" target="_blank" rel="noopener">
<i class="fa-solid fa-location-dot link-card-icon"></i>
<span class="link-card-text">
<span class="link-card-title">Office</span>
<span class="link-card-desc">Office E25A, FLVC Building<br>1753 W Paul Dirac Dr, Tallahassee, FL</span>
</span>
</a>
{% if site.linkedin_username %}
<a class="link-card" href="https://www.linkedin.com/in/{{ site.linkedin_username }}" target="_blank" rel="noopener">
<i class="fa-brands fa-linkedin link-card-icon"></i>
<span class="link-card-text">
<span class="link-card-title">LinkedIn</span>
<span class="link-card-desc">Send me a message</span>
</span>
</a>
{% endif %}
</div>
</div>
