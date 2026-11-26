---
layout: page
title: Gaussian Splatting Digital Twin for Pedestrian Simulation
short_title: Gaussian Splatting Digital Twin
description: A photorealistic 3D reconstruction of a real campus environment, built with Gaussian splatting and populated with simulated pedestrians.
img: /assets/img/project_imgs/gaussian-splat.jpg
category: research
importance: 3
loop: /assets/video/loops/gaussian-splat.mp4
loop_poster: /assets/video/loops/gaussian-splat.jpg
showcase_order: 8
showcase_size: wide
---

## Gaussian Splatting Digital Twin

<!-- TODO: replace this paragraph with a description of the project: how the scene was captured, the splatting pipeline and viewer used, and what the environment is used for. -->
This project reconstructs a real-world campus environment as a photorealistic 3D scene using Gaussian splatting, then places simulated pedestrians into it. The result is a realistic, explorable digital twin for studying pedestrian behavior and interactions with transportation infrastructure.

<div class="row justify-content-sm-center mt-3">
  <div class="col-sm-10">
    <video autoplay loop muted playsinline poster="{{ page.loop_poster | relative_url }}" class="img-fluid rounded z-depth-1" style="width:100%">
      <source src="{{ page.loop | relative_url }}" type="video/mp4">
    </video>
    <div class="caption">Walkthrough of the reconstructed scene with simulated pedestrians (sped up).</div>
  </div>
</div>
