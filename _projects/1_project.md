---
layout: page
title: Standard-Compliant Wi-Fi Sensing with Beamforming Feedback
description: Practical, domain-adaptive, and multi-user sensing with IEEE 802.11 beamforming feedback
img: assets/img/BeamSense.jpg
importance: 1
category: Integrated Sensing and Communication
related_publications: false
---

Wi-Fi sensing can enable applications such as remote healthcare, smart-home monitoring, and human-computer interaction. Most existing systems, however, rely on channel state information (CSI) extracted through specialized hardware or modified firmware—capabilities that are not exposed by standard commercial Wi-Fi devices.

This research program develops a practical alternative based on **beamforming feedback information (BFI)**. BFI is a compressed representation of the wireless channel that is routinely transmitted during IEEE 802.11ac/ax MIMO channel sounding. Because these feedback frames can be captured over the air without modifying the sensing devices, BFI enables standard-compliant sensing with commercial Wi-Fi equipment. It also allows a single monitor to observe the channels between an access point and multiple stations simultaneously.

<div class="row">
  <div class="col-12 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/csi_vs_bfi.jpg" title="Comparison of CSI- and BFI-based Wi-Fi sensing" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Unlike conventional CSI extraction, beamforming feedback can be captured from standard-compliant Wi-Fi transmissions and can expose multiple user channels to a single passive monitor.
</div>

## Research contributions

### Wi-BFI: an open-source extraction tool

[Wi-BFI](https://github.com/kfoysalhaque/Wi-BFI) is the first open-source tool for extracting beamforming feedback angles (BFAs) and reconstructing BFI from captured Wi-Fi frames. It supports IEEE 802.11ac and 802.11ax, 20–160 MHz channels, single-user and multi-user MIMO, and both real-time and offline analysis.

### Understanding compressed MIMO feedback

Our [feedback quantization and grouping study](https://doi.org/10.1109/LWC.2024.3469383) evaluates how BFA quantization and OFDM subchannel grouping affect communication performance across commercial devices, propagation environments, and network configurations. The accompanying [code and datasets](https://github.com/francescamen/MIMO_feedback_quantization_grouping) provide a benchmark for designing efficient feedback mechanisms.

### BFA-Sense: sensing directly from feedback angles

[BFA-Sense](https://doi.org/10.1109/PerComWorkshops59983.2024.10503460) demonstrates that standard-compliant BFAs can support human activity recognition without firmware modifications. Across three subjects, twenty activities, and three environments, BFA-based sensing achieved approximately **11% higher accuracy** than the evaluated CSI-based approach. [Code and data are publicly available](https://github.com/kfoysalhaque/BFA-Sense).

### BeamSense: adapting to unseen domains

[BeamSense](https://doi.org/10.1016/j.comnet.2024.111020) extends BFA sensing with a cross-domain few-shot learning strategy for unseen environments and subjects. It improved accuracy by up to **30%** over the evaluated domain-adaptation baselines and achieved over **98% accuracy** in a gesture-recognition case study. The [implementation and datasets](https://github.com/kfoysalhaque/BeamSense) are open source.

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/Wi-BFI.jpg" title="Wi-BFI system overview" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/BeamSense.jpg" title="BeamSense system overview" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Left: Wi-BFI extracts feedback from devices using different Wi-Fi configurations. Right: BeamSense uses feedback collected from MU-MIMO users for domain-adaptive activity recognition.
</div>

### Si-Fi: simultaneous multi-subject sensing

[Si-Fi](https://www.sciencedirect.com/science/article/pii/S1389128625008734) uses the multi-user nature of BFI to sense several subjects concurrently. In experiments with three subjects performing twenty activities across three environments, Si-Fi achieved up to **99% classification accuracy**. Its few-shot adaptation improved accuracy by up to **27%**, while the system reduced latency by **50%** and channel occupation by **110 KB per sample per sensing device** compared with the evaluated simultaneous multi-subject sensing approach. The [code is available online](https://github.com/kfoysalhaque/Si-FI).

### Open CSI and BFI datasets

To support reproducible research, we released [CSI-BFI-HAR](https://github.com/kfoysalhaque/CSI-BFI-HAR), two human-activity-recognition datasets collected with commercial IEEE 802.11ac devices under line-of-sight and non-line-of-sight conditions. Together, they contain approximately **240 GB of CSI** and **230 GB of BFI**. The data cover twenty activities, six subjects, six experimental setups, and simultaneous multi-subject sensing.

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="lazy" path="assets/img/beamsense_results2.jpg" title="BeamSense comparison and spatial-diversity results" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="lazy" path="assets/img/beamsense_results1.jpg" title="BeamSense cross-domain results" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  BeamSense evaluation across sensing representations, spatial diversity, unseen environments, and unseen subjects.
</div>

## Publications

1. K. F. Haque, F. Meneghello, and F. Restuccia, [“Datasets for Human Activity Recognition with Integrated Sensing and Communications in Wi-Fi”](https://scholar.google.com/citations?view_op=view_citation&hl=en&user=6Ag-9dwAAAAJ&sortby=pubdate&citation_for_view=6Ag-9dwAAAAJ:_Qo2XoVZTnwC), *IEEE Communications Magazine*, 2026. [Code and datasets](https://github.com/kfoysalhaque/CSI-BFI-HAR).
2. K. F. Haque, M. Zhang, F. Meneghello, and F. Restuccia, [“Si-Fi: Learning the Beamforming Feedback for Simultaneous Multi-Subject Sensing”](https://www.sciencedirect.com/science/article/pii/S1389128625008734), *Computer Networks*, 2025. [Code](https://github.com/kfoysalhaque/Si-FI).
3. K. F. Haque, M. Zhang, F. Meneghello, and F. Restuccia, [“BeamSense: Rethinking Wireless Sensing with MU-MIMO Wi-Fi Beamforming Feedback”](https://doi.org/10.1016/j.comnet.2024.111020), *Computer Networks*, 2025. [Code and datasets](https://github.com/kfoysalhaque/BeamSense).
4. F. Meneghello, K. F. Haque, and F. Restuccia, [“Evaluating the Impact of Channel Feedback Quantization and Grouping in IEEE 802.11 MIMO Wi-Fi Networks”](https://doi.org/10.1109/LWC.2024.3469383), *IEEE Wireless Communications Letters*, 2024. [Code and datasets](https://github.com/francescamen/MIMO_feedback_quantization_grouping).
5. K. F. Haque, F. Meneghello, and F. Restuccia, [“BFA-Sense: Learning Beamforming Feedback Angles for Wi-Fi Sensing”](https://doi.org/10.1109/PerComWorkshops59983.2024.10503460), *IEEE PerCom Workshops*, 2024. [Code and data](https://github.com/kfoysalhaque/BFA-Sense).
6. K. F. Haque, F. Meneghello, and F. Restuccia, [“Wi-BFI: Extracting the IEEE 802.11 Beamforming Feedback Information from Commercial Wi-Fi Devices”](https://doi.org/10.1145/3615453.3616514), *ACM WiNTECH*, 2023. [Code](https://github.com/kfoysalhaque/Wi-BFI).
