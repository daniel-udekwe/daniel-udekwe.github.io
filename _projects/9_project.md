---
layout: page
title: Gap-Aware Nonlinear Model Predictive Control for Rigidly Coupled Automated Vehicle Convoys
short_title: Coupled Vehicle Convoys
description: Predictive spacing control that makes rigid couplings between automated vehicles practical.
img: /assets/img/project_imgs/convoy.jpg
category: research
importance: 4
loop: /assets/video/loops/convoy.mp4
loop_poster: /assets/video/loops/convoy.jpg
showcase_order: 1
showcase_size: full
---

**Daniel Udekwe** · Under review

Mechanically coupled convoys of small automated vehicles could offer flexible, rail-like public transport with a human driver in the lead vehicle and automated followers behind. A rigid coupling, however, needs precise coordination between vehicles to avoid transmitting large forces. Earlier work concluded that rigid coupling was impractical; this project shows that the problem lies in the spacing controller, not the coupling.

A nonlinear dynamic bicycle model and its path-coordinate state-space formulations are developed for a two-vehicle convoy. A **gap-aware nonlinear model predictive controller (NMPC)** jointly regulates path tracking and the follower's progress along the leader's shared motion plan, with corrections for communication delay, packet loss and interrupted path updates. It is compared with a proportional-integral (PI) spacing baseline and a soft actor-critic controller.

**Key results**

- Follower spacing error (RMSE) falls from 0.93–1.22 m with PI spacing to about 0.02 m.
- Lateral tracking error falls by a factor of 7–10.
- Spacing error stays below 0.05 m with 300 ms delay and 20% packet loss, and remains stable through a 2 s communication blackout.
- Simulated drawbar forces drop to about 111 N, compared with more than 2 kN under PI spacing.

<div class="row justify-content-sm-center mt-3">
  <div class="col-sm-12">
    <video autoplay loop muted playsinline poster="{{ page.loop_poster | relative_url }}" class="img-fluid rounded z-depth-1" style="width:100%">
      <source src="{{ page.loop | relative_url }}" type="video/mp4">
    </video>
    <div class="caption">Illustration of the two controllers on the same curve, using the paper's reported spacing errors and drawbar forces.</div>
  </div>
</div>
