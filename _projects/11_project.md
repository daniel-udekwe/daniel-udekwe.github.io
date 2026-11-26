---
layout: page
title: "Do Graph Neural Networks Learn Spatial Dependence? Exposure-Informed GeoAI for Statewide Road-Crash Forecasting"
short_title: GeoAI for Crash Forecasting
description: Testing whether graph neural networks truly learn spatial dependence in statewide crash forecasting.
img: /assets/img/project_imgs/geoai-gnn.jpg
category: research
importance: 6
loop: /assets/video/loops/geoai-gnn.mp4
loop_poster: /assets/video/loops/geoai-gnn.jpg
showcase_order: 6
showcase_size: third
---

**Daniel Udekwe, Qianwen (Vivian) Guo** · Under review

Graph neural networks (GNNs) promise better forecasts of processes on networks, but whether they genuinely learn spatial dependence, and whether that improves predictions, is rarely tested. This project examines both for road-crash risk using 855,745 crashes on 201,109 half-mile segments of North Carolina state roads (2021–2024).

A road graph is reconstructed from crash reference fields using training-period data only and validated against known Interstate interchanges. Eleven models, from classical **safety performance functions** to **boosted trees** and **graph-based spatiotemporal networks**, are compared with leakage-free quarterly forecasting, ablations, influence diagnostics, spatial validation and multiple spatial resolutions.

**Key results**

- GNNs reduce residual network autocorrelation by about 40% (Moran's I 0.044–0.054, against 0.073–0.089 for non-graph learners) and improve forecast skill. Both gains vanish when the graph is randomized.
- Learned spatial influence reaches only one hop, while residual dependence extends to four hops. Boosted trees with two-hop spatial lags perform comparably.
- Using test-period crash records to build the graph inflates skill by 0.011–0.014, and spatially held-out validation is 2.5–4 times more variable than random splits.
- The study sets practical evaluation requirements for spatial GeoAI: leakage-free graph construction, strong spatial baselines, dependence diagnostics, spatial validation and multi-scale assessment.

<div class="row justify-content-sm-center mt-3">
  <div class="col-sm-12">
    <video autoplay loop muted playsinline poster="{{ page.loop_poster | relative_url }}" class="img-fluid rounded z-depth-1" style="width:100%">
      <source src="{{ page.loop | relative_url }}" type="video/mp4">
    </video>
    <div class="caption">North Carolina's road network as a graph, with nodes coloured by forecast crash risk. The view zooms into one segment: GNN messages flow in from its directly connected neighbours (1 hop), while residual dependence still links segments up to 4 hops away. The graph is illustrative; the bars show the paper's residual Moran's I by model.</div>
  </div>
</div>
