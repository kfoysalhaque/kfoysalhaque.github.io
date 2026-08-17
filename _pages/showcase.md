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
</style>
