---
layout: page
title: research showcase
permalink: /showcase/
description: Interactive demonstrations of intelligent wireless sensing, communication, and MIMO systems.
nav: true
nav_order: 4
---

<div class="research-showcase">
  <p class="lead">
    Explore working demonstrations of my research in communication-native sensing and AI-driven MIMO systems.
  </p>

  <h2>Featured Demos</h2>

  <div class="demo-entry">
    <h3>BandWeave</h3>
    <p>
      An intelligent MIMO channel-estimation system that fuses observations across frequency bands. BandWeave improves channel acquisition by
      learning complementary propagation information from multiple bands.
    </p>
    <div class="demo-video">
      {% include video.liquid path="https://www.youtube.com/embed/COGgKKtj8SA" title="BandWeave demonstration" %}
    </div>
    <p class="demo-links">
      <a href="{% link _projects/3_intelligent_mimo_systems.md %}">Related project</a>
      &nbsp;&middot;&nbsp;
      <a href="https://ieeexplore.ieee.org/abstract/document/11571725">Paper</a>
      &nbsp;&middot;&nbsp;
      <a href="https://github.com/kfoysalhaque/BandWeave">Code</a>
    </p>
  </div>

  <div class="demo-entry">
    <h3>Wi-BFI</h3>
    <p>
      An open-source Wi-Fi sensing platform that extracts beamforming feedback information from commercial devices, enabling
      protocol-compliant MIMO feedback to support a broad range of integrated sensing and communication applications.
    </p>
    <div class="demo-video">
      {% include video.liquid path="https://www.youtube.com/embed/0k7uYRCmMBw" title="Wi-BFI demonstration" %}
    </div>
    <p class="demo-links">
      <a href="{% link _projects/1_project.md %}">Related project</a>
      &nbsp;&middot;&nbsp;
      <a href="https://doi.org/10.1145/3615453.3616514">Paper</a>
      &nbsp;&middot;&nbsp;
      <a href="https://github.com/kfoysalhaque/Wi-BFI">Code</a>
    </p>
  </div>

  <div class="demo-entry">
    <h3>BeamSense</h3>
    <p>
      Standard-compliant multi-person sensing using beamforming feedback from commercial Wi-Fi devices. BeamSense turns communication-native
      feedback into robust sensing features without requiring specialized sensing hardware.
    </p>
    <div class="demo-video">
      {% include video.liquid path="https://www.youtube.com/embed/U-QTSxG3xpQ" title="BeamSense demonstration" %}
    </div>
    <p class="demo-links">
      <a href="{% link _projects/1_project.md %}">Related project</a>
      &nbsp;&middot;&nbsp;
      <a href="https://doi.org/10.1016/j.comnet.2024.111020">Paper</a>
      &nbsp;&middot;&nbsp;
      <a href="https://github.com/kfoysalhaque/BeamSense">Code</a>
    </p>
  </div>

  <hr class="showcase-divider">

  <h2>Research Datasets</h2>
  <p>
    Public datasets and reproducible pipelines for communication-native sensing and radio fingerprinting across Wi-Fi and mmWave MIMO systems.
  </p>

  <div class="dataset-grid">
    <article class="dataset-card">
      <h3>M3-CFR</h3>
      <p class="dataset-meta">58 GHz mmWave &middot; 8 &times; 8 MIMO CFR &middot; Micro-gestures</p>
      <p>
        A bi-static mmWave MIMO CFR dataset collected with the MAGIC platform for fine-grained recognition under domain shifts. It contains 10
        micro-gesture classes, 3 subjects, 3 indoor environments, 3,000 labeled gesture instances, and approximately 1.5 million CFR frames.
      </p>
      <p class="dataset-links">
        <a href="https://huggingface.co/datasets/foysalhaque/M3-CFR/tree/main">Download dataset</a>
        &nbsp;&middot;&nbsp;
        <a href="https://github.com/kfoysalhaque/M3-CFR">Code &amp; documentation</a>
        &nbsp;&middot;&nbsp;
        <a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=6Ag-9dwAAAAJ&citation_for_view=6Ag-9dwAAAAJ:HDshCWvjkbEC">Paper</a>
      </p>
    </article>

    <article class="dataset-card">
      <h3>CSI-BFI-HAR</h3>
      <p class="dataset-meta">Wi-Fi &middot; Paired CSI and BFI &middot; Human activity recognition</p>
      <p>
        Paired channel state information and beamforming feedback traces for 20 activities. The collection supports single- and simultaneous
        multi-subject recognition across multiple indoor environments, device placements, orientations, and LoS/NLoS conditions.
      </p>
      <p class="dataset-links">
        <a href="https://huggingface.co/datasets/foysalhaque/CSI-BFI-HAR-Dataset">Download dataset</a>
        &nbsp;&middot;&nbsp;
        <a href="https://github.com/kfoysalhaque/CSI-BFI-HAR">Documentation &amp; extraction tools</a>
        &nbsp;&middot;&nbsp;
        <a href="https://ieee-dataport.org/documents/csi-bfi-har-wi-fi-datasets-human-activity-recognition">IEEE DataPort</a>
        &nbsp;&middot;&nbsp;
        <a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=6Ag-9dwAAAAJ&citation_for_view=6Ag-9dwAAAAJ:_Qo2XoVZTnwC">Paper</a>
      </p>
    </article>

    <article class="dataset-card">
      <h3>DeepCSIv2</h3>
      <p class="dataset-meta">Wi-Fi &middot; Compressed MIMO feedback &middot; Radio fingerprinting</p>
      <p>
        A 60.9 GB collection of over-the-air Wi-Fi traces and reconstructed beamforming feedback matrices for physical-layer identification of
        client devices. The release includes raw captures, processed V matrices, extraction tools, and the learning pipeline.
      </p>
      <p class="dataset-links">
        <a href="https://huggingface.co/datasets/foysalhaque/DeepCSIv2/tree/main">Download dataset</a>
        &nbsp;&middot;&nbsp;
        <a href="https://github.com/kfoysalhaque/DeepCSIv2">Code &amp; documentation</a>
        &nbsp;&middot;&nbsp;
        <a href="https://ieeexplore.ieee.org/abstract/document/11152893">Paper</a>
      </p>
    </article>

    <article class="dataset-card">
      <h3>BeamID</h3>
      <p class="dataset-meta">Wi-Fi &middot; MIMO beamforming feedback &middot; Domain adaptation</p>
      <p>
        Complex-valued beamforming feedback measurements for domain-adaptive radio fingerprinting. Organized by client radio and collection
        location, the dataset supports source-domain training and few-shot adaptation to changing deployment environments.
      </p>
      <p class="dataset-links">
        <a href="https://huggingface.co/datasets/foysalhaque/BeamID/tree/main">Download dataset</a>
        &nbsp;&middot;&nbsp;
        <a href="https://github.com/kfoysalhaque/BeamID">Code &amp; documentation</a>
        &nbsp;&middot;&nbsp;
        <a href="https://github.com/kfoysalhaque/BeamID/blob/master/BeamID_NetSoft_2026_archived.pdf">Paper</a>
      </p>
    </article>
  </div>
</div>

<style>
  .research-showcase .lead {
    margin-bottom: 2.5rem;
  }

  .research-showcase .demo-entry {
    margin: 2rem 0 3.5rem;
  }

  .research-showcase .demo-video figure {
    margin: 1.25rem 0 0.75rem;
    position: relative;
    width: 100%;
    padding-top: 56.25%;
    overflow: hidden;
    border-radius: 0.25rem;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.14);
  }

  .research-showcase .demo-video iframe {
    position: absolute;
    inset: 0;
    width: 100%;
    height: 100%;
  }

  .research-showcase .demo-links {
    margin-top: 0.75rem;
    font-weight: 500;
  }

  .research-showcase .showcase-divider {
    margin: 4rem 0 3rem;
  }

  .research-showcase .dataset-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 1.5rem;
    margin-top: 1.5rem;
  }

  .research-showcase .dataset-card {
    display: flex;
    flex-direction: column;
    padding: 1.5rem;
    border: 1px solid var(--global-divider-color);
    border-radius: 0.35rem;
    background: var(--global-card-bg-color);
    box-shadow: 0 3px 10px rgba(0, 0, 0, 0.08);
  }

  .research-showcase .dataset-card h3 {
    margin-top: 0;
  }

  .research-showcase .dataset-meta {
    color: var(--global-theme-color);
    font-weight: 600;
  }

  .research-showcase .dataset-links {
    margin-top: auto;
    padding-top: 0.5rem;
    font-weight: 500;
  }

  @media (max-width: 767px) {
    .research-showcase .dataset-grid {
      grid-template-columns: 1fr;
    }
  }
</style>
