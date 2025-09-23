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

---

<div class="row">
    <div class="col-12 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/csi_vs_bfi.jpg" title="CSI vs BFI Sensing" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    CSI vs proposed Beamforming Feedback based sensing approach
</div>
---

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


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/beamsense_results2.jpg" title="beamsense_results2" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/beamsense_results1.jpg" title="beamsense_results1" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: BeamSense (BFA) vs. SignFi (CSI) and Impact of the spatial diversity of the beamformees on sensing performance
    Right: Comparative analysis of BeamSense with unseen environments, and subjects
</div>

---

### Publications
- Haque, K.F., Meneghello, F. and Restuccia, F., 2023, October. Wi-BFI: Extracting the IEEE 802.11 beamforming feedback information from commercial Wi-Fi devices. In Proceedings of the 17th ACM Workshop on Wireless Network Testbeds, Experimental evaluation & Characterization (pp. 104-111).
- **Feedback Quantization & Grouping** – IEEE WCL 2024 
- **BFA-Sense** – IEEE PerCom Workshops 2024  
- **BeamSense** – Computer Networks 2025 
---