---
layout: page
title: Wi-Fi Sensing in the Wild
description: 
img: assets/img/12.jpg
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

---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/csi_vs_bfi_pipeline.jpg" title="CSI vs BFI/BFA sensing pipeline" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/quantization_tradeoff.jpg" title="Impact of feedback quantization/grouping" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/activity_dataset.jpg" title="Wi-Fi sensing dataset collection setup" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: CSI requires firmware modifications; BFAs are standard-compliant and lightweight.  
    Middle: Quantization and grouping reduce overhead but may affect BER.  
    Right: Our multi-environment activity recognition dataset with Wi-Fi MU-MIMO.
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