---
layout: page
title: Coordinating Human Assistance in Multi-Robot Fleets
short_title: Human Assistance in Multi-Robot Fleets
description: A QUBO framework for joint go, yield and ask decisions.
img: /assets/img/project_imgs/robot-fleet.jpg
category: research
importance: 4
loop: /assets/video/loops/robot-fleet.mp4
loop_poster: /assets/video/loops/robot-fleet.jpg
showcase_order: 6
showcase_size: wide
---

## Coordinating Human Assistance in Multi-Robot Fleets

<!-- TODO: expand this description with the problem setting, method and key results. -->
Sidewalk delivery robots must decide, around uncertain pedestrians, whether to go, yield or ask a remote human operator for help, and operators can only assist a few robots at once. This project formulates those joint go, yield and ask decisions across a robot fleet as a quadratic unconstrained binary optimization (QUBO) problem, so that limited human assistance goes where it is needed most.

<div class="row justify-content-sm-center mt-3">
  <div class="col-sm-10">
    <video autoplay loop muted playsinline poster="{{ page.loop_poster | relative_url }}" class="img-fluid rounded z-depth-1" style="width:100%">
      <source src="{{ page.loop | relative_url }}" type="video/mp4">
    </video>
    <div class="caption">Robots predicting pedestrian crossings and requesting remote operator help (sped up).</div>
  </div>
</div>
