---
layout: page
title: Quantum-Enhanced Reliability Assessment for Schedule-Dependent Public Transit Networks
short_title: Quantum Transit Reliability
description: Quantum amplitude estimation measures whether disrupted neighborhoods can still reach hospitals and shelters by transit.
img: /assets/img/project_imgs/quantum-transit.jpg
category: research
importance: 2
showcase_size: wide
loop: /assets/video/loops/quantum-transit.mp4
loop_poster: /assets/video/loops/quantum-transit.jpg
---

**Daniel Udekwe** · Under review

Public transit is lifeline infrastructure during hurricanes, floods and other emergencies, but its connectivity reliability is hard to quantify: exact evaluation is #P-complete, and Monte Carlo sampling becomes expensive when disconnections are rare. This project presents the first quantum computational framework for connectivity reliability in public transit networks.

Each service link is encoded as a qubit whose amplitudes carry its probability of surviving a disruption, from vehicle breakdowns, cancellations, hazard closures and missed transfers. A reversible quantum circuit propagates reachability through the network, and **quantum amplitude estimation** with **Grover iterations** recovers the probability that a disrupted origin stays connected to critical destinations such as hospitals and shelters. The framework extends two-terminal reliability to K-terminal reliability at an additive O(K) qubit overhead.

**Key results**

- Quantum connectivity decisions match exhaustive classical reachability analysis with zero mismatches across test networks.
- Qiskit simulations reproduce exact reliability values (0.3837 exact vs. 0.3841 estimated on the example network), with the expected quadratic query-complexity advantage over Monte Carlo sampling.
- Sensitivity and intervention analyses rank improvements such as added service frequency, redundancy and emergency contraflow by their effect on reliability.

<div class="row justify-content-sm-center mt-3">
  <div class="col-sm-12">
    <video autoplay loop muted playsinline poster="{{ page.loop_poster | relative_url }}" class="img-fluid rounded z-depth-1" style="width:100%">
      <source src="{{ page.loop | relative_url }}" type="video/mp4">
    </video>
    <div class="caption">The paper's example network. Each link's qubit is in superposition until measured; across many shots, quantum amplitude estimation converges on the reliability with error falling as 1/N, against 1/√N for Monte Carlo. The error curves illustrate the theoretical scaling.</div>
  </div>
</div>
