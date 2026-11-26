---
layout: page
title: "Bilevel Bus Route Design for Older Adults: Benchmarking Quantum, Classical, and Learned Initialization"
short_title: Quantum Bus Route Design (QAOA)
description: A budget-preserving QAOA chooses new bus stops so more older adults can walk to the bus.
img: /assets/img/project_imgs/qaoa-bus.jpg
category: research
importance: 1
loop: /assets/video/loops/qaoa-bus.mp4
loop_poster: /assets/video/loops/qaoa-bus.jpg
showcase_order: 2
showcase_size: wide
---

**Daniel Udekwe, Ruimin Ke, Qianwen Guo** · Under review

Improving public transportation for older adults means balancing shorter walks to the bus against efficient bus operations. This project models that trade-off as a bilevel problem: a planner selects additional bus stops to minimize residents' perceived walking and in-vehicle time, while the operator chooses the shortest feasible route through them.

A **budget-preserving Quantum Approximate Optimization Algorithm (QAOA)** generates the starting population for a genetic algorithm. Its initial Dicke state and XY mixer only ever sample stop sets that respect the stop budget, so no penalty terms are needed. The framework is benchmarked against classical and reinforcement-learning-based initializers on 226 real bus-segment instances built from GTFS, OpenStreetMap and demographic data in Tallahassee, Florida (23,400 benchmark runs).

**Key results**

- Optimized designs increase the share of older adults within 400 m of a bus stop by a median of 3.4 percentage points and cut perceived travel time by 4.8%.
- Budget-preserving QAOA needs fewer objective evaluations than penalty-based simulated annealing in 81% of matched runs.
- A classical constraint-preserving sampler does better still, showing the gains come mainly from constraint-preserving sampling. This sets a rigorous classical benchmark for future quantum optimization methods.

<div class="row justify-content-sm-center mt-3">
  <div class="col-sm-12">
    <video autoplay loop muted playsinline poster="{{ page.loop_poster | relative_url }}" class="img-fluid rounded z-depth-1" style="width:100%">
      <source src="{{ page.loop | relative_url }}" type="video/mp4">
    </video>
    <div class="caption">A budget-preserving QAOA simulated on a small example with 8 candidate stops and a budget of 3. As layers are added, probability concentrates on the best stop set, which reroutes the bus to reach more older adults.</div>
  </div>
</div>
