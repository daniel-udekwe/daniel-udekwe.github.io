---
layout: page
title: Media
permalink: /media/
description: Conferences, demos and outreach.
nav: false
nav_order: 3
# Gallery items, newest first. category: conference, outreach or lab.
# Images live in assets/img/media_imgs/web/ (resized to 1400 px for fast loading).
gallery:
  - { img: trb-podium.jpg, category: conference, title: "Podium presentation", event: "TRB Annual Meeting" }
  - { img: fav-2026-ask-or-act.jpg, category: conference, title: "Ask or Act poster", event: "Florida Automated Vehicles Summit · November 2026" }
  - { img: qc2026-qaoa-poster.jpg, category: conference, title: "Quantum bus route design poster", event: "QC2026, Vanderbilt University · August 2026" }
  - { img: trb2026-vrise-poster.jpg, category: conference, title: "VRISE poster", event: "105th TRB Annual Meeting · January 2026" }
  - { img: trb2026-bike-simulator.jpg, category: conference, title: "VR cycling simulator", event: "105th TRB Annual Meeting · January 2026" }
  - { img: trb2026-driving-simulator.jpg, category: conference, title: "VR driving simulator", event: "105th TRB Annual Meeting · January 2026" }
  - { img: media_9.jpg, category: conference, title: "Presentation", event: "2025 INFORMS Annual Meeting · 28 October 2025" }
  - { img: media_10.jpg, category: conference, title: "Presentation", event: "2025 INFORMS Annual Meeting · 28 October 2025" }
  - { img: media_7.jpg, category: conference, title: "Conference session", event: "2025 INFORMS Annual Meeting · 27 October 2025" }
  - { img: media_8.jpg, category: conference, title: "Conference session", event: "2025 INFORMS Annual Meeting · 27 October 2025" }
  - { img: edge-fair-vr-lidar.jpg, category: outreach, title: "VR and LiDAR demos", event: "FAMU-FSU College of Engineering EDGE Fair" }
  - { img: media_3.jpg, category: outreach, title: "Research showcase", event: "FAMU-FSU College of Engineering EDGE Fair · 17 September 2025" }
  - { img: mediaa_4.jpg, category: outreach, title: "Public demonstration", event: "Leon County Public Safety Complex · 9 April 2025" }
  - { img: mediaa_5.jpg, category: outreach, title: "Public demonstration", event: "Leon County Public Safety Complex · 9 April 2025" }
  - { img: media_6.jpg, category: outreach, title: "Public demonstration", event: "Leon County Public Safety Complex · 9 April 2025" }
  - { img: first-outreach-vr.jpg, category: outreach, title: "VR demo for young students", event: "STEM outreach at a FIRST Robotics event" }
  - { img: media_1.jpg, category: conference, title: "Poster session", event: "104th TRB Annual Meeting · 9 January 2025" }
  - { img: media_2.jpg, category: conference, title: "Poster session", event: "104th TRB Annual Meeting · 9 January 2025" }
  - { video: turtlebot-hallway.mp4, img: turtlebot-hallway.jpg, category: lab, title: "TurtleBot3 navigating a hallway", event: "Ask or Act robot navigation experiments" }
  - { img: turtlebot3.jpg, category: lab, title: "TurtleBot3 research robot", event: "Robot navigation under uncertain human intent" }
  - { img: leveling-rod.jpg, category: lab, title: "Differential leveling equipment", event: "Surveying lab, FAMU-FSU College of Engineering" }
  - { img: automotive-lab-tour.jpg, category: lab, title: "Automotive lab tour", event: "Vehicle research facility visit" }
  - { img: rider-vr-development.jpg, category: lab, title: "Building VR environments", event: "RIDER Center, FAMU-FSU College of Engineering" }
  - { img: vr-demo-visitor.jpg, category: lab, title: "VR demo for a visitor", event: "Driving simulator lab" }
  - { img: driving-simulator-lab.jpg, category: lab, title: "Driving simulator study", event: "Driving simulator lab" }
---

<div class="media-filters" role="tablist">
  <button class="media-chip active" data-filter="all">All</button>
  <button class="media-chip" data-filter="conference">Conferences</button>
  <button class="media-chip" data-filter="outreach">Outreach</button>
  <button class="media-chip" data-filter="lab">In the lab</button>
</div>

<div class="media-masonry">
{% for item in page.gallery %}
<figure class="media-item" data-category="{{ item.category }}">
{% if item.video %}<video src="{{ '/assets/img/media_imgs/web/' | append: item.video | relative_url }}" poster="{{ '/assets/img/media_imgs/web/' | append: item.img | relative_url }}" autoplay loop muted playsinline aria-label="{{ item.title }}"></video>{% else %}<img src="{{ '/assets/img/media_imgs/web/' | append: item.img | relative_url }}" alt="{{ item.title }}, {{ item.event }}" loading="lazy">{% endif %}
<figcaption><span class="media-title">{{ item.title }}</span><span class="media-event">{{ item.event }}</span></figcaption>
</figure>
{% endfor %}
</div>

<div class="media-lightbox" aria-hidden="true">
  <button class="media-close" aria-label="Close">&times;</button>
  <button class="media-prev" aria-label="Previous">&#8249;</button>
  <figure><img alt=""><video autoplay loop muted playsinline controls></video><figcaption></figcaption></figure>
  <button class="media-next" aria-label="Next">&#8250;</button>
</div>

<script>
(function () {
  const items = Array.from(document.querySelectorAll('.media-item'));
  const chips = document.querySelectorAll('.media-chip');
  chips.forEach(c => c.addEventListener('click', () => {
    chips.forEach(x => x.classList.remove('active')); c.classList.add('active');
    const f = c.dataset.filter;
    items.forEach(it => { it.style.display = (f === 'all' || it.dataset.category === f) ? '' : 'none'; });
  }));
  const lb = document.querySelector('.media-lightbox'), img = lb.querySelector('img'), vid = lb.querySelector('video'), cap = lb.querySelector('figcaption');
  let cur = 0;
  const visible = () => items.filter(it => it.style.display !== 'none');
  function show(i) {
    const v = visible(); cur = (i + v.length) % v.length; const it = v[cur];
    const v2 = it.querySelector('video');
    if (v2) { img.style.display = 'none'; vid.style.display = ''; vid.src = v2.src; vid.play(); }
    else { vid.pause(); vid.style.display = 'none'; img.style.display = ''; img.src = it.querySelector('img').src; img.alt = it.querySelector('img').alt; }
    cap.innerHTML = it.querySelector('figcaption').innerHTML;
    lb.classList.add('open'); lb.setAttribute('aria-hidden', 'false');
  }
  items.forEach(it => it.addEventListener('click', () => show(visible().indexOf(it))));
  lb.querySelector('.media-close').addEventListener('click', () => { lb.classList.remove('open'); vid.pause(); });
  lb.querySelector('.media-prev').addEventListener('click', e => { e.stopPropagation(); show(cur - 1); });
  lb.querySelector('.media-next').addEventListener('click', e => { e.stopPropagation(); show(cur + 1); });
  lb.addEventListener('click', e => { if (e.target === lb) lb.classList.remove('open'); });
  document.addEventListener('keydown', e => {
    if (!lb.classList.contains('open')) return;
    if (e.key === 'Escape') lb.classList.remove('open');
    if (e.key === 'ArrowLeft') show(cur - 1);
    if (e.key === 'ArrowRight') show(cur + 1);
  });
})();
</script>
