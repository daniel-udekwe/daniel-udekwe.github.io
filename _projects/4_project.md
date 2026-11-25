---
layout: page
title: Finite Element Crash Simulation of Vehicle–Pedestrian and Vehicle–Vehicle Impacts
short_title: Vehicle Crash Simulation
description: Finite element simulations of pedestrian and side-impact collisions, used to study occupant and pedestrian injury risk.
img: /assets/img/project_imgs/crash.jpg
category: research
importance: 1
loops:
  - src: /assets/video/loops/crash-ped-front.mp4
    poster: /assets/video/loops/crash-ped-front.jpg
    label: Pedestrian impact, front
  - src: /assets/video/loops/crash-ped-rear.mp4
    poster: /assets/video/loops/crash-ped-rear.jpg
    label: Pedestrian impact, rear
  - src: /assets/video/loops/crash-side-1.mp4
    poster: /assets/video/loops/crash-side-1.jpg
    label: Side impact
  - src: /assets/video/loops/crash-side-2.mp4
    poster: /assets/video/loops/crash-side-2.jpg
    label: Oblique side impact
---

## Vehicle Crash Simulation

<!-- TODO: replace this paragraph with a description of the project: software used, vehicle and pedestrian models, what was measured, and key findings. -->
This project uses finite element crash simulations to analyze how vehicles and pedestrians deform during collisions. The scenarios include a pedestrian struck at the front and rear of an SUV, and two vehicle-to-vehicle side impacts. Color contours highlight regions of high stress and deformation.

<div class="row mt-3">
  {% for clip in page.loops %}
    <div class="col-sm-6 mt-3">
      <video autoplay loop muted playsinline poster="{{ clip.poster | relative_url }}" class="img-fluid rounded z-depth-1" style="width:100%">
        <source src="{{ clip.src | relative_url }}" type="video/mp4">
      </video>
      <div class="caption">{{ clip.label }} (sped up)</div>
    </div>
  {% endfor %}
</div>
