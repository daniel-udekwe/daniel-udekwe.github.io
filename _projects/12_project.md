---
layout: page
title: "Forecasting Traffic Across Hurricane Landfall: A Rolling-Origin Evaluation of Route-Choice Features and Training Strategies"
short_title: Hurricane Evacuation Traffic Forecasting
description: Forecasting evacuation traffic through Hurricane Sally's landfall, and what actually improves the forecasts.
img: /assets/img/project_imgs/hurricane-sally.jpg
category: research
importance: 7
loop: /assets/video/loops/hurricane-sally.mp4
loop_poster: /assets/video/loops/hurricane-sally.jpg
showcase_order: 7
showcase_size: full
---

**Daniel Udekwe, Qianwen Guo, Eren Erman Ozguven, Alican Sevim, Xiao Huang, Yadong Wang, Adolf K.Y. Ng** · Under review

Accurate traffic prediction during hurricane evacuations supports emergency management, but the value of learned traveler-behavior representations is unclear. This project tests whether route-choice features learned by an **adversarial behavior component inspired by Adversarial Inverse Reinforcement Learning (AIRL)** improve evacuation forecasts, and how much the results depend on how the forecaster is trained.

Using INRIX probe-vehicle trajectories on four Escambia County, Florida corridors (I-10, US 98, US 90 and FL 97) during Hurricane Sally (2020), route-choice probabilities, entropy and maximum transition probability are estimated and added to **LSTM** and ridge speed forecasts (15–90 minutes ahead). A **rolling-origin evaluation** forecasts each day from September 8 to 26, spanning landfall on September 16.

**Key results**

- During the acute evacuation period, AIRL-inspired features reduce pooled-LSTM error by 1.06–1.21 kph, but simple empirical-transition features perform as well or better.
- Training strategy matters far more: pretraining on 2019 and fine-tuning on 2020 reduces error by 1.9–2.3 kph, and training on 2019 alone by 4.1–4.5 kph.
- Route-choice information offers limited predictive value; the training data matters most.

<div class="row justify-content-sm-center mt-3">
  <div class="col-sm-12">
    <video autoplay loop muted playsinline poster="{{ page.loop_poster | relative_url }}" class="img-fluid rounded z-depth-1" style="width:100%">
      <source src="{{ page.loop | relative_url }}" type="video/mp4">
    </video>
    <div class="caption">A 3D coastal corridor through three phases of Hurricane Sally: evacuation queues, an empty road at landfall, and recovered two-way traffic. Vehicle movements come from a SUMO microsimulation of an illustrative corridor; the speed series is illustrative, and the bars show the paper's reported error reductions. 3D models by Kenney (CC0).</div>
  </div>
</div>
