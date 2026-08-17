---
layout: page
title: MIMO Feedback for Radio Fingerprinting
description: Domain-adaptive device identification from standard-compliant Wi-Fi beamforming feedback
img: assets/img/beamid_overview.png
importance: 1
category: AI-Driven Wireless Security
related_publications: false
---

Reliable device identification is essential for monitoring and securing dense wireless networks. Cryptographic authentication can establish device credentials, but it requires key distribution and does not directly reveal whether the transmitting radio hardware matches the claimed identity. Radio fingerprinting provides a complementary physical-layer signal by learning the small, device-specific impairments introduced during radio manufacturing.

This research demonstrates that those hardware signatures propagate into the **compressed MIMO channel feedback** routinely transmitted by commercial Wi-Fi stations. Because beamforming feedback frames are standard-compliant and can be captured passively over the air, they enable device identification without firmware modification, dedicated probing signals, or direct access to the client.

## BeamID: fingerprinting across environments

[BeamID](https://scholar.google.com/citations?view_op=view_citation&hl=en&user=6Ag-9dwAAAAJ&sortby=pubdate&citation_for_view=6Ag-9dwAAAAJ:hC7cP41nSMkC) addresses the central practical limitation of radio fingerprinting: a model trained in one propagation environment often fails when the device moves to a new location. Channel variations alter the measured feedback and can overwhelm the much smaller hardware signature.

BeamID learns client-discriminative representations through supervised contrastive learning and performs lightweight few-shot alignment directly in the embedding space. This preserves separation between radios while adapting the representation to a new environment without retraining the complete model.

The framework was evaluated using measurements from **15 commercial Wi-Fi network interface cards across nine locations**. With only **five labeled samples per client** in an unseen environment, BeamID achieved up to approximately **99% identification accuracy** and required only approximately **2.3 seconds** for adaptation. The [implementation and data](https://github.com/kfoysalhaque/BeamID) are publicly available.

<div class="row">
  <div class="col-12 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/beamid_overview.png" title="BeamID domain-adaptive radio-fingerprinting pipeline" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  BeamID aggregates reconstructed MIMO feedback matrices, learns radio-discriminative embeddings in a source environment, and adapts those embeddings before identifying clients in a new domain.
</div>

## DeepCSIv2: identifying Wi-Fi stations from compressed feedback

[DeepCSIv2](https://ieeexplore.ieee.org/abstract/document/11152893) establishes that standard Wi-Fi channel sounding exposes stable station-specific information. Hardware impairments introduced while a station estimates the channel percolate into its compressed and quantized CSI feedback. A neural architecture extracts these subtle patterns and identifies the station that generated the feedback.

The study evaluated **18 nominally identical IEEE 802.11ax network interface cards** under changes in propagation environment and operating bandwidth. DeepCSIv2 achieved more than **96% identification accuracy**, showing that devices of the same model and manufacturer can be distinguished through passively captured MIMO control traffic.

<div class="row">
  <div class="col-12 mt-3 mt-md-0">
    {% include figure.liquid loading="lazy" path="assets/img/deepcsiv2_overview.png" title="DeepCSIv2 passive Wi-Fi station fingerprinting" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  DeepCSIv2 reconstructs compressed MIMO feedback captured over the air and learns the physical-layer fingerprint of each Wi-Fi station.
</div>

## Publications

1. K. F. Haque, F. Meneghello, and F. Restuccia, [“BeamID: Domain-Adaptive Radio Fingerprinting with MIMO Beamforming Feedback”](https://scholar.google.com/citations?view_op=view_citation&hl=en&user=6Ag-9dwAAAAJ&sortby=pubdate&citation_for_view=6Ag-9dwAAAAJ:hC7cP41nSMkC), *IEEE NetSoft*, 2026. [Code and data](https://github.com/kfoysalhaque/BeamID).
2. F. Meneghello, K. F. Haque, and F. Restuccia, [“Radio Fingerprinting of Wi-Fi Devices Through MIMO Compressed Channel Feedback”](https://ieeexplore.ieee.org/abstract/document/11152893), *IEEE INFOCOM Workshops*, 2025.
