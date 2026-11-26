---
layout: page
title: Modeling Sun-Glare Crash Risk with Solar Geometry, Street-View Data, and Exposure-Based Safety Performance Functions
short_title: Sun-Glare Crash Risk
description: Solar geometry and street-view imagery quantify how low sun aligned with the road raises crash risk.
img: /assets/img/project_imgs/sun-glare.jpg
category: research
importance: 5
loop: /assets/video/loops/sun-glare.mp4
loop_poster: /assets/video/loops/sun-glare.jpg
showcase_order: 5
showcase_size: wide
---

**Daniel Udekwe, Zhipeng Deng, Xiao Huang, Eren Erman Ozguven, Ren Moses, Qianwen Guo** · Under review

Sun glare impairs driver visibility, but its contribution to crashes is hard to quantify because police record it inconsistently. This project builds an exposure-based framework that combines **solar geometry**, driver-level validation, **machine learning**, **street-view image segmentation** and **safety performance modeling**.

Glare exposure was reconstructed for 1.47 million police-reported North Carolina crashes (2021–2024) from each driver's heading and the sun's position, and validated against 8,559 drivers that officers coded as blinded by sunlight.

**Key results**

- Officer-coded glare rates rise steadily as the sun lines up with the driving direction, reaching 16.7%, about 40 times the daytime average, when the sun is within 5° of the heading and below 10° elevation.
- On a held-out year, a gradient-boosted model identified 54.5% of officer-coded glare drivers, against 42.8% for a fixed angular rule.
- Street-view obstruction filtering agreed strongly with manual labels (Cohen's κ = 0.855).
- Each additional 100 hours a year of solar alignment raises glare crashes by 17% (IRR = 1.17, 95% CI 1.16–1.19). The resulting exposure measure, crash modification factor and Empirical Bayes screening help agencies prioritize sites for countermeasures.

<div class="row justify-content-sm-center mt-3">
  <div class="col-sm-12">
    <video autoplay loop muted playsinline poster="{{ page.loop_poster | relative_url }}" class="img-fluid rounded z-depth-1" style="width:100%">
      <source src="{{ page.loop | relative_url }}" type="video/mp4">
    </video>
    <div class="caption">As the sun drops toward the driver's line of sight, glare washes out the road ahead. The bars show the paper's officer-coded glare rates for each sun–heading angle band.</div>
  </div>
</div>
