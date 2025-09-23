---
layout: page
title: Wi-Fi Sensing in the Wild
description: 
img: assets/img/BeamSense.jpg
importance: 1
category: Integrated Sensing and Communication
related_publications: true
---

Wi-Fi networks are everywhere – but beyond connectivity, they can also sense.  
In this project, we rethink Wi-Fi sensing by leveraging **standard-compliant MU-MIMO beamforming feedback** (BFI/BFA) rather than proprietary or firmware-hacked CSI.  
Our work spans four major contributions:

- **Wi-BFI**: The first open-source tool to extract BFAs/BFI in the wild
- **Feedback Quantization & Grouping**: A benchmark study on how IEEE 802.11 feedback compression affects performance  
- **BFA-Sense**: A learning framework for sensing directly from BFAs, no firmware hacks required
- **BeamSense**: A robust, cross-domain few-shot sensing system that outperforms CSI-based methods
ß
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Wi-BFI.jpg" title="Wi-BFI Overview" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/BeamSense.jpg" title="BeamSense Overview" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: Wi-BFI can concurrently extract BFAs from devices operating with different standards, channels, and bandwidths.  
    Right: BeamSense, a new approach to Wi-Fi sensing where the standard-compliant BFAs routinely sent in MU-MIMO Wi-Fi networks is used to characterize the propagation environment between the MU-MIMO users and the AP
</div>

---

Unlike CSI-based approaches, which require **specialized tools** and only capture single-user links,  
BFA-based sensing allows us to **capture all MU-MIMO channels simultaneously**, dramatically improving spatial diversity.  
We demonstrated that sensing with BFAs achieves **10% higher accuracy** than CSI approaches, and with our cross-domain adaptation (FAMReS), accuracy improves by **up to 30%** on unseen environments

<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/beamsense_results.jpg" title="BeamSense accuracy across domains" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/gesture_recognition.jpg" title="Gesture recognition with BFAs" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
    Left: BeamSense outperforms CSI-based baselines in cross-environment sensing.  
    Right: BFAs enable gesture recognition with over 98% accuracy.
</div>

---

### Publications
- **Wi-BFI** – ACM WiNTECH 2023
- **Feedback Quantization & Grouping** – IEEE WCL 2024 
- **BFA-Sense** – IEEE PerCom Workshops 2024  
- **BeamSense** – Computer Networks 2025 
---