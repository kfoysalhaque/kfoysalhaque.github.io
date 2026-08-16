---
layout: page
title: mmWave and Sub-THz Integrated Sensing and Communication
description: Communication-native micro-gesture recognition and material sensing across mmWave and sub-THz systems
img: assets/img/magic_overview.png
importance: 2
category: Integrated Sensing and Communication
related_publications: false
---

Millimeter-wave (mmWave) and sub-terahertz (sub-THz) systems offer wide bandwidths and high spatial resolution, making them powerful platforms for integrated sensing and communication (ISAC). Much of the existing work at these frequencies, however, relies on dedicated radar signals and sensing-specific hardware. This research program instead uses measurements produced by communication systems—including MIMO channel frequency response (CFR)—to support fine-grained sensing without a separate radar infrastructure.

Across **MAGIC**, **M3-CFR**, and **SCOPE**, we develop communication-native sensing systems and datasets for two challenging applications: micro-gesture recognition and material classification. The work also addresses a central obstacle in wireless sensing: maintaining reliable performance when subjects, environments, distances, and hardware configurations change.

## MAGIC: domain-adaptive mmWave gesture recognition

[MAGIC](https://doi.org/10.1109/WoWMoM65615.2025.00030) uses high-resolution CFR extracted from a fully digital mmWave MIMO communication system instead of radar measurements. Its temporal convolutional network captures long-range gesture dynamics, while the Adaptive Temporal Embedding Network (ATEN) uses meta-learning to adapt the model to unseen subjects and environments with limited additional data.

The system was evaluated using ten micro-gestures performed by two subjects in three environments. MAGIC achieved **99.24% baseline accuracy** and maintained up to **98.82% accuracy under domain adaptation**, outperforming the evaluated state-of-the-art adaptation methods by **14% on average**. The [code and dataset](https://github.com/kfoysalhaque/MAGIC) are publicly available.

<div class="row">
  <div class="col-12 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/magic_overview.png" title="MAGIC gesture-recognition workflow" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  MAGIC estimates mmWave CFR during MIMO channel sounding, constructs a domain-adaptive dataset, and learns to recognize fine-grained gestures through its TCN and ATEN architecture.
</div>

## M3-CFR: a communication-native mmWave sensing dataset

[M3-CFR](https://doi.org/10.1109/LSENS.2026.3703644) provides a bistatic mmWave MIMO CFR dataset designed specifically for studying sensing under domain shifts. It was collected with an **8 × 8 fully digital MIMO testbed operating at 58 GHz with 1 GHz bandwidth**.

The dataset contains **3,000 labeled gesture instances** and approximately **1.5 million CFR frames**, covering ten micro-gestures, three subjects, and three indoor environments. Alongside the raw CFR, M3-CFR provides domain-adaptively processed data using path-loss compensation, frequency normalization, and entropy-guided subchannel filtering. This makes it possible to benchmark cross-environment and cross-subject sensing directly from communication waveforms. The [dataset and code](https://github.com/kfoysalhaque/M3-CFR) are openly available.

<div class="row">
  <div class="col-12 mt-3 mt-md-0">
    {% include figure.liquid loading="lazy" path="assets/img/m3cfr_dataset.png" title="M3-CFR experimental setup and data collection" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  M3-CFR uses a bistatic 8 × 8 mmWave MIMO testbed and synchronized video ground truth to capture micro-gestures across multiple subjects and environments.
</div>

## SCOPE: cooperative sub-THz material sensing

[SCOPE](https://doi.org/10.1109/LWC.2025.3576010) extends communication-native sensing to sub-THz frequencies. Rather than relying only on reflected signals, SCOPE jointly analyzes signals that **penetrate through** and **reflect from** a material. An entropy-weighted ensemble combines the complementary information from the two propagation paths.

The system was implemented on a real sub-THz testbed with **10 GHz bandwidth** and evaluated across different sensing distances, antenna gains, and channel conditions. Spatial Variability Augmentation (SVA) improves generalization across these configurations. SCOPE achieved up to **99% accuracy** when distinguishing five materials: glass, wood, metal, air, and plastic. The [implementation and dataset](https://github.com/kfoysalhaque/SCOPE) are publicly available.

<div class="row">
  <div class="col-12 mt-3 mt-md-0">
    {% include figure.liquid loading="lazy" path="assets/img/scope_overview.png" title="SCOPE cooperative material-sensing workflow" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  SCOPE estimates CFR from penetrating and reflected sub-THz signals, trains specialized models for both paths, and combines their predictions through entropy-weighted ensembling.
</div>

## Publications

1. K. F. Haque, F. Meneghello, and F. Restuccia, [“M3-CFR: A Domain-Adaptive Bi-Static mmWave MIMO CFR Dataset for Micro-Gesture Recognition”](https://doi.org/10.1109/LSENS.2026.3703644), *IEEE Sensors Letters*, 2026. [Code and dataset](https://github.com/kfoysalhaque/M3-CFR).
2. K. F. Haque, X. Cantos-Roman, F. Meneghello, J. M. Jornet, and F. Restuccia, [“SCOPE: Cooperative Integrated Communications and Sensing for Material Classification at Sub-Terahertz Frequencies”](https://doi.org/10.1109/LWC.2025.3576010), *IEEE Wireless Communications Letters*, 2025. [Code and dataset](https://github.com/kfoysalhaque/SCOPE).
3. K. F. Haque, K. M. Rumman, A. Elyasi, F. Meneghello, and F. Restuccia, [“MAGIC: Meta-Learning Adaptive Gesture Recognition with mmWave MIMO CSI”](https://doi.org/10.1109/WoWMoM65615.2025.00030), *IEEE WoWMoM*, 2025. [Code and dataset](https://github.com/kfoysalhaque/MAGIC).
