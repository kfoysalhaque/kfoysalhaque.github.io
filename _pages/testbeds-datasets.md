---
layout: page
title: testbeds & datasets
permalink: /testbeds-datasets/
description: Experimental wireless platforms and public datasets supporting reproducible systems research.
nav: true
nav_order: 5
---

<div class="testbeds-datasets">
  <p class="lead">
    Public datasets and reproducible pipelines for communication-native sensing and radio fingerprinting across Wi-Fi and mmWave MIMO systems.
  </p>

  <h2>Research Datasets</h2>

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
  .testbeds-datasets .lead {
    margin-bottom: 2.5rem;
  }

  .testbeds-datasets .dataset-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 1.5rem;
    margin-top: 1.5rem;
  }

  .testbeds-datasets .dataset-card {
    display: flex;
    flex-direction: column;
    padding: 1.5rem;
    border: 1px solid var(--global-divider-color);
    border-radius: 0.35rem;
    background: var(--global-card-bg-color);
    box-shadow: 0 3px 10px rgba(0, 0, 0, 0.08);
  }

  .testbeds-datasets .dataset-card h3 {
    margin-top: 0;
  }

  .testbeds-datasets .dataset-meta {
    color: var(--global-theme-color);
    font-weight: 600;
  }

  .testbeds-datasets .dataset-links {
    margin-top: auto;
    padding-top: 0.5rem;
    font-weight: 500;
  }

  @media (max-width: 767px) {
    .testbeds-datasets .dataset-grid {
      grid-template-columns: 1fr;
    }
  }
</style>
