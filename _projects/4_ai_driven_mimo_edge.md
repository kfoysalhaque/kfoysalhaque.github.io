---
layout: page
title: AI-Driven MIMO for Wireless Edge Computing
description: Sensing-assisted, task-aware, and physical-layer intelligence for efficient edge inference
img: assets/img/sawec_overview.png
importance: 2
category: AI-Driven MIMO
related_publications: false
---

Wireless edge computing allows mobile and embedded devices to execute demanding AI workloads at nearby edge servers. Yet conventional systems often treat communication and inference as separate problems: devices transmit complete inputs through the network stack, even when only a small part of the data affects the application outcome. This creates avoidable channel occupancy, latency, computation, and energy consumption.

This research program uses wireless sensing, MIMO resource adaptation, and physical-layer learning to make edge communication **aware of the task being executed**. The central contribution is **SAWEC**, which uses information sensed from the wireless channel to identify and offload only relevant regions of high-resolution visual data. PhyDNNs and SOAR extend this principle by moving AI inference into the physical layer and adapting MU-MIMO resources to task-specific reliability requirements.

## SAWEC: sensing-assisted wireless edge computing

[SAWEC](https://doi.org/10.48550/arXiv.2402.10021) rethinks visual edge offloading by using wireless sensing to understand where meaningful changes occur in the physical environment. Instead of transmitting every complete video frame, SAWEC estimates the angle and time of arrival of wireless multipath components, tracks environmental changes, maps them to regions of interest (ROIs) in the camera view, and sends only those regions to the edge server.

The framework consists of three stages:

1. **Sensing-assisted ROI detection:** Wi-Fi channel measurements localize and track moving objects in the environment.
2. **Selective ROI offloading:** only the portions of a frame containing relevant changes are transmitted.
3. **Edge task execution:** the server performs computer-vision inference on high-resolution ROIs rather than compressed full frames.

SAWEC was evaluated with a **10K 360° camera** and a **160 MHz Wi-Fi 6 sensing system** performing localization and tracking. Experiments covered an anechoic chamber and an entrance hall, two subjects, and six deployment configurations, with instance segmentation and object detection as downstream tasks. SAWEC reduced both **channel occupation and end-to-end latency by more than 90%** while improving task performance relative to the evaluated wireless edge-computing approaches. The [implementation and datasets](https://github.com/kfoysalhaque/SAWEC) are publicly available.

<div class="row">
  <div class="col-12 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/sawec_overview.png" title="SAWEC sensing-assisted edge-computing workflow" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  SAWEC senses environmental changes, maps them to visual regions of interest, selectively offloads those regions, and executes the AI task at the edge server.
</div>

## PhyDNNs: executing neural networks at the physical layer

[PhyDNNs](https://doi.org/10.1109/INFOCOM55648.2025.11044671) eliminates another major source of edge-computing overhead: repeatedly encapsulating and decapsulating intermediate DNN features through the conventional network protocol stack. It adapts pretrained neural networks to emit and consume physical-layer waveforms directly, jointly optimizing communication efficiency and task performance.

Experiments with a Jetson Orin Nano, software-defined radios, and the Colosseum wireless network emulator showed that PhyDNNs reduced end-to-end inference latency by up to **48×**, transmitted data by **1,385×**, and mobile-device power consumption by **13×**, while keeping accuracy within 7% of the evaluated baselines. It also achieved **4.3× lower latency** than the evaluated task-oriented JSCC method with only a 1.79% performance loss. The [implementation](https://github.com/AbdiMohammad/PhyDistInf) is open source.

<div class="row">
  <div class="col-12 mt-3 mt-md-0">
    {% include figure.liquid loading="lazy" path="assets/img/phydnns_overview.png" title="Conventional distributed inference and the PhyDNN physical-layer approach" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  PhyDNNs replaces conventional protocol-stack transport of latent features with neural-network representations transmitted directly as physical-layer waveforms.
</div>

## SOAR: semantic MU-MIMO resource adaptation

[SOAR](https://doi.org/10.1109/DCOSS-IoT65416.2025.00014) makes MU-MIMO edge offloading aware of both operating context and application reliability. A context-aware distributional deep reinforcement learning agent selects transmission configurations that satisfy task-specific packet-loss objectives while minimizing radio-resource use.

SOAR was evaluated for image classification and instance segmentation in a real vehicular system under line-of-sight and non-line-of-sight conditions. By adapting the number of antennas, spatial streams, and bandwidth to the task and environment, it reduced resource utilization by **35–40%** compared with fixed-configuration benchmarks. The [SOAR code](https://github.com/Restuccia-Group/SOAR) is publicly available.

<div class="row">
  <div class="col-12 mt-3 mt-md-0">
    {% include figure.liquid loading="lazy" path="assets/img/soar_overview.png" title="SOAR task-oriented MU-MIMO offloading" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  SOAR adapts MU-MIMO communication resources to maintain task reliability across changing wireless contexts, instead of relying on a fixed transmission configuration.
</div>

## Publications

1. K. F. Haque, F. Meneghello, M. E. Karim, and F. Restuccia, [“SAWEC: Sensing-Assisted Wireless Edge Computing”](https://doi.org/10.48550/arXiv.2402.10021), 2024. [Code and datasets](https://github.com/kfoysalhaque/SAWEC).
2. K. F. Haque, F. Meneghello, and F. Restuccia, [“Integrated Sensing and Communication for Efficient Edge Computing”](https://doi.org/10.1109/WiMob61911.2024.10770523), *IEEE WiMob*, 2024. [Code and datasets](https://github.com/kfoysalhaque/SAWEC).
3. M. Abdi, K. F. Haque, F. Meneghello, J. Ashdown, and F. Restuccia, [“PhyDNNs: Bringing Deep Neural Networks to the Physical Layer”](https://doi.org/10.1109/INFOCOM55648.2025.11044671), *IEEE INFOCOM*, 2025. [Code](https://github.com/AbdiMohammad/PhyDistInf).
4. S. L. G. Contreras, K. F. Haque, F. Restuccia, and M. Levorato, [“SOAR: Semantic Multi-User MIMO Communications for Reliable Wireless Edge Computing”](https://doi.org/10.1109/DCOSS-IoT65416.2025.00014), *IEEE DCOSS-IoT*, 2025. [Code](https://github.com/Restuccia-Group/SOAR).
