---
layout: page
title: demos & talks
permalink: /showcase/
description: Demonstrations and presentations of intelligent wireless sensing, communication, and MIMO systems.
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

  <h2>Selected Talks</h2>
  <p>Conference presentations highlighting recent work in AI-driven MIMO systems.</p>

  <div class="talk-grid">
    <article class="talk-card">
      <img
        src="{{ '/assets/img/talks/beamid_netsoft_2026.png' | relative_url }}"
        alt="Title slide for the BeamID presentation at IEEE NetSoft 2026"
        loading="lazy"
      >
      <div class="talk-content">
        <p class="talk-venue">IEEE NetSoft 2026 &middot; 23 slides</p>
        <h3>BeamID: Domain-Adaptive Radio Fingerprinting with MIMO Beamforming Feedback</h3>
        <p>
          Domain-adaptive learning turns standard-compliant MIMO beamforming feedback into reliable client fingerprints across changing
          environments.
        </p>
        <p class="talk-links">
          <a href="{{ '/assets/slides/BeamID_NetSoft_2026.pptx' | relative_url }}">Download slides</a>
          &nbsp;&middot;&nbsp;
          <a href="{% link _projects/5_mimo_radio_fingerprinting.md %}">Project</a>
          &nbsp;&middot;&nbsp;
          <a href="https://github.com/kfoysalhaque/BeamID/blob/master/BeamID_NetSoft_2026_archived.pdf">Paper</a>
          &nbsp;&middot;&nbsp;
          <a href="https://github.com/kfoysalhaque/BeamID">Code &amp; data</a>
        </p>
      </div>
    </article>

    <article class="talk-card">
      <img
        src="{{ '/assets/img/talks/bandweave_infocom_2026.png' | relative_url }}"
        alt="Title slide for the BandWeave presentation at IEEE INFOCOM 2026"
        loading="lazy"
      >
      <div class="talk-content">
        <p class="talk-venue">IEEE INFOCOM 2026 &middot; 36 slides</p>
        <p class="talk-award">Best Paper Award</p>
        <h3>BANDWEAVE: Enhanced Channel Estimation in MIMO Networks with Multi-Band Fusion</h3>
        <p>
          Multi-band CFR fusion uncovers complementary multipath information to improve MIMO channel estimation and communication performance.
        </p>
        <p class="talk-links">
          <a href="{{ '/assets/slides/BandWeave_INFOCOM_2026.pptx' | relative_url }}">Download slides</a>
          &nbsp;&middot;&nbsp;
          <a href="{% link _projects/3_intelligent_mimo_systems.md %}">Project</a>
          &nbsp;&middot;&nbsp;
          <a href="https://ieeexplore.ieee.org/abstract/document/11571725">Paper</a>
          &nbsp;&middot;&nbsp;
          <a href="https://github.com/kfoysalhaque/BandWeave">Code</a>
        </p>
      </div>
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

  .research-showcase .talk-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 1.5rem;
    margin-top: 1.5rem;
  }

  .research-showcase .talk-card {
    display: flex;
    flex-direction: column;
    overflow: hidden;
    border: 1px solid var(--global-divider-color);
    border-radius: 0.35rem;
    background: var(--global-card-bg-color);
    box-shadow: 0 3px 10px rgba(0, 0, 0, 0.08);
  }

  .research-showcase .talk-card > img {
    width: 100%;
    aspect-ratio: 16 / 9;
    object-fit: contain;
    background: #292d2f;
    border-bottom: 1px solid var(--global-divider-color);
  }

  .research-showcase .talk-content {
    display: flex;
    flex: 1;
    flex-direction: column;
    padding: 1.25rem;
  }

  .research-showcase .talk-content h3 {
    margin-top: 0.25rem;
  }

  .research-showcase .talk-venue {
    margin-bottom: 0;
    color: var(--global-theme-color);
    font-weight: 600;
  }

  .research-showcase .talk-award {
    align-self: flex-start;
    margin: 0.6rem 0 0;
    padding: 0.15rem 0.55rem;
    border-radius: 1rem;
    color: #fff;
    background: var(--global-theme-color);
    font-size: 0.82rem;
    font-weight: 600;
  }

  .research-showcase .talk-links {
    margin-top: auto;
    padding-top: 0.5rem;
    font-weight: 500;
  }

  @media (max-width: 767px) {
    .research-showcase .talk-grid {
      grid-template-columns: 1fr;
    }
  }

</style>
