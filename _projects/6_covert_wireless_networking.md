---
layout: page
title: Energy-Efficient Covert Wireless Networking
description: Decentralized multi-modal routing that jointly optimizes energy, throughput, and covertness
img: assets/img/decor_overview.jpg
importance: 2
category: AI-Driven Wireless Security
related_publications: false
---

Covert wireless communication aims to prevent an adversary from detecting that a transmission is taking place. In multi-hop heterogeneous networks, this creates a difficult three-way tradeoff: stricter covertness limits transmit power, throughput requirements demand sufficient link capacity, and poorly coordinated routes can consume excessive energy.

This research develops decentralized routing mechanisms that exploit multiple available communication modalities simultaneously. Rather than selecting a single frequency or wireless technology for every link, the proposed methods jointly choose modalities, transmit powers, and routes to satisfy covertness and throughput constraints with substantially lower energy consumption.

## DECOR: scalable cluster-based covert routing

[DECOR](https://ieeexplore.ieee.org/abstract/document/11450432) is a decentralized, energy-efficient covert-routing framework for heterogeneous wireless networks. It combines:

1. **Link-level optimization:** selects the communication modalities and transmit powers that minimize per-link energy while meeting throughput and detection-error constraints.
2. **Energy-aware clustering:** groups nodes using multi-modal channel conditions and selects cluster heads using residual energy and connectivity.
3. **Network-level routing:** computes an energy-efficient end-to-end path through a custom cluster-based link-state routing protocol.
4. **Adaptive re-evaluation:** updates clusters and routes when channel conditions change while avoiding unnecessary network-wide control exchanges.

The cluster-based design distributes routing decisions while reducing the signaling required to maintain a global network view. Numerical evaluations show that DECOR achieves up to **23.5× improvement in energy consumption** over single-modality baselines and up to **12× reduction in routing overhead** compared with the evaluated state-of-the-art approach.

<div class="row">
  <div class="col-12 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/decor_overview.jpg" title="DECOR adaptive cluster-based routing workflow" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  DECOR initializes clusters and routes during the first cycle, then performs localized re-evaluation and route updates only when significant channel changes occur.
</div>

## DEER: simultaneous multi-modal covert routing

[DEER](https://doi.org/10.1109/WCNC61545.2025.10978544) establishes the multi-modal routing foundation. It jointly optimizes the transmit powers of multiple wireless modalities at each hop, then applies a decentralized Dijkstra-based link-state routing procedure to minimize end-to-end power while satisfying covertness and throughput requirements.

Numerical analysis shows that DEER improved energy efficiency by **23.5×** relative to the evaluated single-modality baseline and by **2.9×** relative to a naïve simultaneous multi-modal strategy. The results demonstrate that coordinated use of heterogeneous links can increase throughput while consuming less energy and preserving the required level of covertness.

<div class="row">
  <div class="col-12 mt-3 mt-md-0">
    {% include figure.liquid loading="lazy" path="assets/img/deer_overview.jpg" title="DEER simultaneous multi-modal covert routing" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Unlike single-modality routing, DEER combines multiple communication technologies along a route to improve throughput and energy efficiency under an adversary’s detection constraint.
</div>

## Publications

1. K. F. Haque, J. H. Kong, T. J. Moore, K. Chan, F. Restuccia, and F. T. Dagefu, [“DECOR: Multi-Modal Decentralized Cluster-Based Energy-Efficient Covert Routing in HetNets”](https://ieeexplore.ieee.org/abstract/document/11450432), *IEEE Transactions on Information Forensics and Security*, vol. 21, 2026.
2. K. F. Haque, J. Kong, T. J. Moore, F. Restuccia, and F. T. Dagefu, [“DEER: Simultaneous Multi-Modal Decentralized Energy-Efficient Covert Routing”](https://doi.org/10.1109/WCNC61545.2025.10978544), *IEEE WCNC*, 2025.
