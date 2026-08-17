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
    Experimental wireless platforms and public datasets for reproducible research across Wi-Fi and mmWave MIMO systems.
  </p>

  <h2>Experimental Testbeds</h2>

  <article class="testbed-card">
    <img
      src="{{ '/assets/img/testbeds/sub6_isac_testbed.png' | relative_url }}"
      alt="Sub-6 GHz Wi-Fi ISAC testbed with distributed CSI and BFI capture stations"
      loading="eager"
    >
    <div class="testbed-content">
      <h3>Sub-6 GHz Wi-Fi ISAC Testbed</h3>
      <p class="testbed-meta">IEEE 802.11ac/ax &middot; CSI &amp; BFI &middot; SU/MU-MIMO &middot; Commercial Wi-Fi</p>
      <p>
        A configurable multi-node Wi-Fi ISAC platform for comparative collection of uncompressed Channel State Information (CSI) and
        standards-compliant compressed Beamforming Feedback Information (BFI). Distributed capture stations support controlled sensing
        experiments across devices, subjects, locations, orientations, and LoS/NLoS conditions.
      </p>

      <div class="testbed-details">
        <section>
          <h4>Measurement Stack</h4>
          <ul>
            <li>
              <strong>CSI:</strong> Powered by <a href="https://github.com/seemoo-lab/nexmon_csi">Nexmon CSI</a> for per-frame channel
              measurements from supported Broadcom Wi-Fi chipsets.
            </li>
            <li>
              <strong>BFI:</strong> Powered by <a href="https://github.com/kfoysalhaque/Wi-BFI">Wi-BFI</a> for extracting beamforming feedback
              angles and reconstructing feedback matrices from IEEE 802.11ac/ax frames.
            </li>
          </ul>
        </section>

        <section>
          <h4>Research Enabled</h4>
          <ul>
            <li>Single- and multi-subject Wi-Fi sensing</li>
            <li>Cross-environment domain adaptation</li>
            <li>CSI-versus-BFI sensing comparisons</li>
            <li>Beamforming-feedback radio fingerprinting</li>
            <li>BeamSense, Si-FI, and CSI-BFI-HAR</li>
          </ul>
        </section>
      </div>
    </div>
  </article>

  <article class="testbed-card">
    <div class="testbed-gallery">
      <img
        src="{{ '/assets/img/testbeds/wisec_testbed.png' | relative_url }}"
        alt="WiSEC 6 by 6 sub-6 GHz MIMO testbed supported by 18 IEEE 802.11ax network interface cards"
        loading="lazy"
      >
      <img
        src="{{ '/assets/img/testbeds/wisec_hardware.jpg' | relative_url }}"
        alt="WiSEC hardware with reconfigurable antenna array and live channel measurements"
        loading="lazy"
      >
    </div>
    <div class="testbed-content">
      <h3>WiSEC: Multiband Wi-Fi Sensing and Communication Testbed</h3>
      <p class="testbed-meta">18 IEEE 802.11ax NICs &middot; 36 antennas &middot; 2.4/5/6 GHz &middot; Up to 160 MHz</p>
      <p>
        A modular COTS Wi-Fi platform for large-scale multi-antenna and multiband experimentation. WiSEC integrates 18 independently
        configurable Intel NICs with two antennas each; the NICs can operate as separate devices or be combined into larger MIMO
        configurations, including a reconfigurable 6 &times; 6 antenna array.
      </p>

      <div class="testbed-details">
        <section>
          <h4>System Capabilities</h4>
          <ul>
            <li>Independent operation across the 2.4, 5, and 6 GHz Wi-Fi bands</li>
            <li>Reconfigurable antenna geometries and distributed MU-MIMO deployments</li>
            <li>CSI and BFI acquisition from ongoing or triggered Wi-Fi transmissions</li>
            <li>Simultaneous real-time collection and processing with onboard compute</li>
          </ul>
        </section>

        <section>
          <h4>Research Enabled</h4>
          <ul>
            <li>BeamID and DeepCSIv2 radio fingerprinting</li>
            <li>Large-scale beamforming and MU-MIMO evaluation</li>
            <li>Multiband MIMO sensing and communication</li>
            <li>AI-driven channel analysis and domain adaptation</li>
          </ul>
        </section>
      </div>
    </div>
  </article>

  <hr class="section-divider">

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

  .testbeds-datasets .testbed-card {
    overflow: hidden;
    margin-top: 1.5rem;
    border: 1px solid var(--global-divider-color);
    border-radius: 0.35rem;
    background: var(--global-card-bg-color);
    box-shadow: 0 3px 10px rgba(0, 0, 0, 0.08);
  }

  .testbeds-datasets .testbed-card > img {
    display: block;
    width: 100%;
    height: auto;
    border-bottom: 1px solid var(--global-divider-color);
  }

  .testbeds-datasets .testbed-gallery {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 1px;
    background: var(--global-divider-color);
    border-bottom: 1px solid var(--global-divider-color);
  }

  .testbeds-datasets .testbed-gallery img {
    display: block;
    width: 100%;
    height: 100%;
    aspect-ratio: 16 / 9;
    object-fit: cover;
    background: var(--global-card-bg-color);
  }

  .testbeds-datasets .testbed-content {
    padding: 1.5rem;
  }

  .testbeds-datasets .testbed-content h3 {
    margin-top: 0;
  }

  .testbeds-datasets .testbed-meta {
    color: var(--global-theme-color);
    font-weight: 600;
  }

  .testbeds-datasets .testbed-details {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 2rem;
    margin-top: 1.25rem;
  }

  .testbeds-datasets .testbed-details h4 {
    margin-bottom: 0.75rem;
  }

  .testbeds-datasets .testbed-details ul {
    margin-bottom: 0;
    padding-left: 1.25rem;
  }

  .testbeds-datasets .section-divider {
    margin: 4rem 0 3rem;
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
    .testbeds-datasets .testbed-details,
    .testbeds-datasets .testbed-gallery,
    .testbeds-datasets .dataset-grid {
      grid-template-columns: 1fr;
    }
  }
</style>
