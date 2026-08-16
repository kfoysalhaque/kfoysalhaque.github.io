---
layout: page
title: Intelligent MIMO Systems
description: Learning-based channel estimation, compression, and adaptive feedback for efficient MIMO networks
img: assets/img/bandweave_overview.jpg
importance: 1
category: AI-Driven MIMO
related_publications: false
---

Multiple-input multiple-output (MIMO) networks depend on accurate and timely channel knowledge. In practice, acquiring that knowledge introduces substantial overhead: channel estimates are compressed, transmitted over limited feedback links, and quickly become outdated as propagation conditions change. Measurements from a single frequency band may also hide important multipath components through frequency-selective destructive interference.

This research program develops **intelligent channel-acquisition mechanisms** that improve what channel information is measured, how efficiently it is represented, and when it should be transmitted. The work spans multi-band channel fusion, learning-driven feedback scheduling, and experimental analysis of standardized MIMO feedback compression.

## BANDWEAVE: learning to fuse channels across bands

[BANDWEAVE](https://ieeexplore.ieee.org/abstract/document/11571725)—recipient of the [Best Paper Award at IEEE INFOCOM 2026](https://infocom2026.ieee-infocom.org/awards)—is a multi-band CFR fusion framework that reconstructs a more complete view of the wireless channel from complementary observations across frequency bands. Unlike spectrum-aggregation methods designed primarily for sensing or localization, BANDWEAVE directly optimizes channel estimates for end-to-end communication performance.

Its progressive learning pipeline has three phases:

1. **Supervised pretraining** learns a shared multi-band channel representation.
2. **Simulation-in-the-loop fine-tuning** connects the learned representation to physical-layer metrics such as bit error rate (BER).
3. **Online feedback-aware adaptation** adjusts the fusion policy as propagation conditions change.

BANDWEAVE was evaluated on an IEEE 802.11ac MU-MIMO Wi-Fi testbed and a 60 GHz mmWave MIMO platform across three propagation environments. It delivered more than **16% improvement in throughput and BER**, achieved over **4.9× communication-performance gain** relative to the evaluated band-merging approaches, and reduced inference time and energy consumption by up to **17×** and **18×**, respectively, on resource-constrained edge platforms. The [implementation is open source](https://github.com/kfoysalhaque/BandWeave).

<div class="row">
  <div class="col-12 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/bandweave_overview.jpg" title="BANDWEAVE multi-band channel-fusion workflow" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  BANDWEAVE combines CFRs from multiple contiguous or non-contiguous bands, progressively learns a communication-aware fusion policy, and feeds the enhanced channel estimate back for MIMO precoding.
</div>

## SHRINK: feedback only when the channel requires it

IEEE 802.11 channel sounding normally requests feedback at fixed intervals, even when the wireless channel is stable. [SHRINK](https://doi.org/10.1145/3704413.3764421) replaces this rigid behavior with a data-driven sounding policy. Each station analyzes its current and previous channel estimates, predicts the resulting throughput variation, and decides whether to transmit updated feedback or a lightweight negative acknowledgment.

Experiments with commercial Wi-Fi devices—including measurements in an anechoic chamber and dynamic indoor environments—showed that SHRINK:

- Reduced feedback airtime and data overhead by **81% on average** without degrading precoding performance.
- Improved overhead reduction by **33.6% on average** over the evaluated state-of-the-art approaches.
- Increased throughput by **24.5%** through more efficient use of channel airtime.

The [SHRINK implementation](https://github.com/RummaN38/SHRINK_MobiHoc) is publicly available.

<div class="row">
  <div class="col-12 mt-3 mt-md-0">
    {% include figure.liquid loading="lazy" path="assets/img/shrink_overview.jpg" title="SHRINK adaptive channel-sounding procedure" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  SHRINK predicts whether reusing the previous feedback will affect throughput and transmits a new compressed channel estimate only when necessary.
</div>

## Quantization and grouping in standardized MIMO feedback

Before optimizing when feedback should be sent, it is essential to understand how standardized compression changes the channel representation itself. Our [IEEE 802.11 feedback study](https://doi.org/10.1109/LWC.2024.3469383) systematically evaluates beamforming-angle quantization and OFDM subchannel grouping in IEEE 802.11ac/ax networks.

The evaluation combines channel measurements from commercial devices with standards-compliant emulation across multiple MIMO configurations, bandwidths, modulation and coding schemes, and propagation environments. It characterizes the tradeoff between feedback overhead, beamforming-matrix reconstruction error, and BER, providing an experimental benchmark for future compression and channel-acquisition strategies. The [datasets and emulation framework](https://github.com/francescamen/MIMO_feedback_quantization_grouping) are publicly available.

<div class="row">
  <div class="col-12 mt-3 mt-md-0">
    {% include figure.liquid loading="lazy" path="assets/img/mimo_feedback_results.jpg" title="Impact of MIMO feedback quantization on reconstruction error and BER" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Experimental evaluation of beamforming-feedback reconstruction error and BER across IEEE 802.11ac/ax configurations and propagation environments.
</div>

## Publications

1. K. F. Haque, F. Meneghello, J. Ashdown, and F. Restuccia, [“BANDWEAVE: Enhanced Channel Estimation in MIMO Networks with Multi-Band Fusion”](https://ieeexplore.ieee.org/abstract/document/11571725), *IEEE INFOCOM*, 2026. **Best Paper Award.** [Code](https://github.com/kfoysalhaque/BandWeave).
2. K. M. Rumman, F. Meneghello, K. F. Haque, F. Gringoli, and F. Restuccia, [“SHRINK: Reducing MIMO Feedback Overhead in Wi-Fi with Dynamic Data-Driven Channel Sounding”](https://doi.org/10.1145/3704413.3764421), *ACM MobiHoc*, 2025. [Code](https://github.com/RummaN38/SHRINK_MobiHoc).
3. F. Meneghello, K. F. Haque, and F. Restuccia, [“Evaluating the Impact of Channel Feedback Quantization and Grouping in IEEE 802.11 MIMO Wi-Fi Networks”](https://doi.org/10.1109/LWC.2024.3469383), *IEEE Wireless Communications Letters*, 2024. [Code and datasets](https://github.com/francescamen/MIMO_feedback_quantization_grouping).
