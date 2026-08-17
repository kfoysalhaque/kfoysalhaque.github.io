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
        <p class="talk-venue">IEEE NetSoft 2026</p>
        <h3>BeamID: Domain-Adaptive Radio Fingerprinting with MIMO Beamforming Feedback</h3>
        <p>
          Domain-adaptive learning turns standard-compliant MIMO beamforming feedback into reliable client fingerprints across changing
          environments.
        </p>
        <p class="talk-links">
          <button
            type="button"
            class="slide-viewer-trigger"
            data-dialog="beamid-slide-viewer"
            data-pdf="{{ '/assets/slides/BeamID_NetSoft_2026.pdf' | relative_url }}"
          >Browse slides</button>
          &nbsp;&middot;&nbsp;
          <a href="{{ '/assets/slides/BeamID_NetSoft_2026.pptx' | relative_url }}">Download PowerPoint</a>
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
        <p class="talk-venue">IEEE INFOCOM 2026</p>
        <p class="talk-award">Best Paper Award</p>
        <h3>BANDWEAVE: Enhanced Channel Estimation in MIMO Networks with Multi-Band Fusion</h3>
        <p>
          Multi-band CFR fusion uncovers complementary multipath information to improve MIMO channel estimation and communication performance.
        </p>
        <p class="talk-links">
          <button
            type="button"
            class="slide-viewer-trigger"
            data-dialog="bandweave-slide-viewer"
            data-pdf="{{ '/assets/slides/BandWeave_INFOCOM_2026.pdf' | relative_url }}"
          >Browse slides</button>
          &nbsp;&middot;&nbsp;
          <a href="{{ '/assets/slides/BandWeave_INFOCOM_2026.pptx' | relative_url }}">Download PowerPoint</a>
          &nbsp;&middot;&nbsp;
          <a href="{% link _projects/3_intelligent_mimo_systems.md %}">Project</a>
          &nbsp;&middot;&nbsp;
          <a href="https://ieeexplore.ieee.org/abstract/document/11571725">Paper</a>
          &nbsp;&middot;&nbsp;
          <a href="https://github.com/kfoysalhaque/BandWeave">Code</a>
        </p>
      </div>
    </article>

    <article class="talk-card">
      <img
        src="{{ '/assets/img/talks/sawec_research_talk.png' | relative_url }}"
        alt="Title slide for the SAWEC research presentation"
        loading="lazy"
      >
      <div class="talk-content">
        <p class="talk-venue">Research Talk &middot; SAWEC</p>
        <h3>SAWEC: Sensing-Assisted Wireless Edge Computing</h3>
        <p>
          Wireless sensing identifies relevant regions in high-resolution visual data, enabling selective edge offloading that reduces channel
          occupation and end-to-end latency by more than 90%.
        </p>
        <p class="talk-links">
          <button
            type="button"
            class="slide-viewer-trigger"
            data-dialog="sawec-slide-viewer"
            data-pdf="{{ '/assets/slides/SAWEC_Research_Talk.pdf' | relative_url }}"
          >Browse slides</button>
          &nbsp;&middot;&nbsp;
          <a href="{{ '/assets/slides/SAWEC_Research_Talk.pptx' | relative_url }}">Download PowerPoint</a>
          &nbsp;&middot;&nbsp;
          <a href="{% link _projects/4_ai_driven_mimo_edge.md %}">Project</a>
          &nbsp;&middot;&nbsp;
          <a href="https://doi.org/10.48550/arXiv.2402.10021">Paper</a>
          &nbsp;&middot;&nbsp;
          <a href="https://github.com/kfoysalhaque/SAWEC">Code &amp; data</a>
        </p>
      </div>
    </article>

    <article class="talk-card">
      <img
        src="{{ '/assets/img/talks/deer_wcnc_2025.png' | relative_url }}"
        alt="Title slide for the DEER presentation at IEEE WCNC 2025"
        loading="lazy"
      >
      <div class="talk-content">
        <p class="talk-venue">IEEE WCNC 2025</p>
        <h3>DEER: Simultaneous Multi-Modal Decentralized Energy-Efficient Covert Routing</h3>
        <p>
          Decentralized routing across multiple wireless modalities jointly addresses covertness, throughput, and energy efficiency in
          heterogeneous networks.
        </p>
        <p class="talk-links">
          <button
            type="button"
            class="slide-viewer-trigger"
            data-dialog="deer-slide-viewer"
            data-pdf="{{ '/assets/slides/DEER_WCNC_2025.pdf' | relative_url }}"
          >Browse slides</button>
          &nbsp;&middot;&nbsp;
          <a href="{{ '/assets/slides/DEER_WCNC_2025.pptx' | relative_url }}">Download PowerPoint</a>
          &nbsp;&middot;&nbsp;
          <a href="{% link _projects/6_covert_wireless_networking.md %}">Project</a>
          &nbsp;&middot;&nbsp;
          <a href="https://doi.org/10.1109/WCNC61545.2025.10978544">Paper</a>
        </p>
      </div>
    </article>

    <article class="talk-card">
      <img
        src="{{ '/assets/img/talks/beamsense_research_talk.png' | relative_url }}"
        alt="Title slide for the BeamSense research presentation"
        loading="lazy"
      >
      <div class="talk-content">
        <p class="talk-venue">Research Talk &middot; BeamSense</p>
        <h3>BeamSense: Rethinking Wireless Sensing with MU-MIMO Wi-Fi Beamforming Feedback</h3>
        <p>
          Standard-compliant beamforming feedback enables adaptable Wi-Fi sensing on commercial devices without firmware modifications or
          specialized sensing hardware.
        </p>
        <p class="talk-links">
          <button
            type="button"
            class="slide-viewer-trigger"
            data-dialog="beamsense-slide-viewer"
            data-pdf="{{ '/assets/slides/BeamSense_Research_Talk.pdf' | relative_url }}"
          >Browse slides</button>
          &nbsp;&middot;&nbsp;
          <a href="{{ '/assets/slides/BeamSense_Research_Talk.pptx' | relative_url }}">Download PowerPoint</a>
          &nbsp;&middot;&nbsp;
          <a href="{% link _projects/1_project.md %}">Project</a>
          &nbsp;&middot;&nbsp;
          <a href="https://doi.org/10.1016/j.comnet.2024.111020">Paper</a>
          &nbsp;&middot;&nbsp;
          <a href="https://github.com/kfoysalhaque/BeamSense">Code &amp; data</a>
        </p>
      </div>
    </article>

    <article class="talk-card">
      <img
        src="{{ '/assets/img/talks/magic.png' | relative_url }}"
        alt="Title slide for the MAGIC presentation at IEEE WoWMoM 2025"
        loading="lazy"
      >
      <div class="talk-content">
        <p class="talk-venue">IEEE WoWMoM 2025</p>
        <h3>MAGIC: Meta-Learning Adaptive Gesture Recognition with mmWave MIMO CSI</h3>
        <p>
          Communication-native mmWave MIMO channel measurements and meta-learning enable fine-grained micro-gesture recognition that adapts
          to new subjects and environments.
        </p>
        <p class="talk-links">
          <button
            type="button"
            class="slide-viewer-trigger"
            data-dialog="magic-slide-viewer"
            data-pdf="{{ '/assets/slides/MAGIC.pdf' | relative_url }}"
          >Browse slides</button>
          &nbsp;&middot;&nbsp;
          <a href="{{ '/assets/slides/MAGIC.pptx' | relative_url }}">Download PowerPoint</a>
          &nbsp;&middot;&nbsp;
          <a href="{% link _projects/2_mmwave_subthz_isac.md %}">Project</a>
          &nbsp;&middot;&nbsp;
          <a href="https://doi.org/10.1109/WoWMoM65615.2025.00030">Paper</a>
          &nbsp;&middot;&nbsp;
          <a href="https://github.com/kfoysalhaque/MAGIC">Code &amp; data</a>
        </p>
      </div>
    </article>

    <article class="talk-card">
      <img
        src="{{ '/assets/img/talks/wi_bfi_wintech_2023.png' | relative_url }}"
        alt="Title slide for the Wi-BFI presentation at ACM WiNTECH 2023"
        loading="lazy"
      >
      <div class="talk-content">
        <p class="talk-venue">ACM WiNTECH 2023</p>
        <h3>Wi-BFI: Extracting IEEE 802.11 Beamforming Feedback Information from Commercial Wi-Fi Devices</h3>
        <p>
          Wi-BFI extracts beamforming feedback angles from IEEE 802.11ac/ax frames and reconstructs compressed channel information for
          real-time and offline wireless experimentation.
        </p>
        <p class="talk-links">
          <button
            type="button"
            class="slide-viewer-trigger"
            data-dialog="wi-bfi-slide-viewer"
            data-pdf="{{ '/assets/slides/Wi-BFI_WiNTECH_2023.pdf' | relative_url }}"
          >Browse slides</button>
          &nbsp;&middot;&nbsp;
          <a href="{{ '/assets/slides/Wi-BFI_WiNTECH_2023.pptx' | relative_url }}">Download PowerPoint</a>
          &nbsp;&middot;&nbsp;
          <a href="{% link _projects/1_project.md %}">Project</a>
          &nbsp;&middot;&nbsp;
          <a href="https://doi.org/10.1145/3615453.3616514">Paper</a>
          &nbsp;&middot;&nbsp;
          <a href="https://github.com/kfoysalhaque/Wi-BFI">Code</a>
        </p>
      </div>
    </article>
  </div>

  <dialog id="beamid-slide-viewer" class="slide-dialog">
    <div class="slide-dialog-header">
      <strong>BeamID — IEEE NetSoft 2026</strong>
      <form method="dialog"><button aria-label="Close slide viewer">&times;</button></form>
    </div>
    <iframe
      data-src="{{ '/assets/slides/BeamID_NetSoft_2026.pdf' | relative_url }}#view=FitH"
      title="Browse the BeamID presentation slides"
    ></iframe>
    <a class="slide-dialog-link" href="{{ '/assets/slides/BeamID_NetSoft_2026.pdf' | relative_url }}" target="_blank" rel="noopener">
      Open PDF in a new tab
    </a>
  </dialog>

  <dialog id="bandweave-slide-viewer" class="slide-dialog">
    <div class="slide-dialog-header">
      <strong>BANDWEAVE — IEEE INFOCOM 2026</strong>
      <form method="dialog"><button aria-label="Close slide viewer">&times;</button></form>
    </div>
    <iframe
      data-src="{{ '/assets/slides/BandWeave_INFOCOM_2026.pdf' | relative_url }}#view=FitH"
      title="Browse the BANDWEAVE presentation slides"
    ></iframe>
    <a class="slide-dialog-link" href="{{ '/assets/slides/BandWeave_INFOCOM_2026.pdf' | relative_url }}" target="_blank" rel="noopener">
      Open PDF in a new tab
    </a>
  </dialog>

  <dialog id="sawec-slide-viewer" class="slide-dialog">
    <div class="slide-dialog-header">
      <strong>SAWEC — Research Talk</strong>
      <form method="dialog"><button aria-label="Close slide viewer">&times;</button></form>
    </div>
    <iframe
      data-src="{{ '/assets/slides/SAWEC_Research_Talk.pdf' | relative_url }}#view=FitH"
      title="Browse the SAWEC presentation slides"
    ></iframe>
    <a class="slide-dialog-link" href="{{ '/assets/slides/SAWEC_Research_Talk.pdf' | relative_url }}" target="_blank" rel="noopener">
      Open PDF in a new tab
    </a>
  </dialog>

  <dialog id="deer-slide-viewer" class="slide-dialog">
    <div class="slide-dialog-header">
      <strong>DEER — IEEE WCNC 2025</strong>
      <form method="dialog"><button aria-label="Close slide viewer">&times;</button></form>
    </div>
    <iframe
      data-src="{{ '/assets/slides/DEER_WCNC_2025.pdf' | relative_url }}#view=FitH"
      title="Browse the DEER presentation slides"
    ></iframe>
    <a class="slide-dialog-link" href="{{ '/assets/slides/DEER_WCNC_2025.pdf' | relative_url }}" target="_blank" rel="noopener">
      Open PDF in a new tab
    </a>
  </dialog>

  <dialog id="beamsense-slide-viewer" class="slide-dialog">
    <div class="slide-dialog-header">
      <strong>BeamSense — Research Talk</strong>
      <form method="dialog"><button aria-label="Close slide viewer">&times;</button></form>
    </div>
    <iframe
      data-src="{{ '/assets/slides/BeamSense_Research_Talk.pdf' | relative_url }}#view=FitH"
      title="Browse the BeamSense presentation slides"
    ></iframe>
    <a class="slide-dialog-link" href="{{ '/assets/slides/BeamSense_Research_Talk.pdf' | relative_url }}" target="_blank" rel="noopener">
      Open PDF in a new tab
    </a>
  </dialog>

  <dialog id="wi-bfi-slide-viewer" class="slide-dialog">
    <div class="slide-dialog-header">
      <strong>Wi-BFI — ACM WiNTECH 2023</strong>
      <form method="dialog"><button aria-label="Close slide viewer">&times;</button></form>
    </div>
    <iframe
      data-src="{{ '/assets/slides/Wi-BFI_WiNTECH_2023.pdf' | relative_url }}#view=FitH"
      title="Browse the Wi-BFI presentation slides"
    ></iframe>
    <a class="slide-dialog-link" href="{{ '/assets/slides/Wi-BFI_WiNTECH_2023.pdf' | relative_url }}" target="_blank" rel="noopener">
      Open PDF in a new tab
    </a>
  </dialog>

  <dialog id="magic-slide-viewer" class="slide-dialog">
    <div class="slide-dialog-header">
      <strong>MAGIC — IEEE WoWMoM 2025</strong>
      <form method="dialog"><button aria-label="Close slide viewer">&times;</button></form>
    </div>
    <iframe
      data-src="{{ '/assets/slides/MAGIC.pdf' | relative_url }}#view=FitH"
      title="Browse the MAGIC presentation slides"
    ></iframe>
    <a class="slide-dialog-link" href="{{ '/assets/slides/MAGIC.pdf' | relative_url }}" target="_blank" rel="noopener">
      Open PDF in a new tab
    </a>
  </dialog>

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

  .research-showcase .slide-viewer-trigger {
    display: inline;
    margin: 0;
    padding: 0;
    border: 0;
    color: var(--global-theme-color);
    background: transparent;
    font: inherit;
    cursor: pointer;
  }

  .research-showcase .slide-viewer-trigger:hover {
    color: var(--global-hover-color);
    text-decoration: underline;
  }

  .research-showcase .slide-dialog {
    width: min(1100px, 96vw);
    height: 92vh;
    padding: 0;
    border: 1px solid var(--global-divider-color);
    border-radius: 0.4rem;
    color: var(--global-text-color);
    background: var(--global-bg-color);
    box-shadow: 0 12px 36px rgba(0, 0, 0, 0.35);
  }

  .research-showcase .slide-dialog::backdrop {
    background: rgba(0, 0, 0, 0.72);
  }

  .research-showcase .slide-dialog[open] {
    display: flex;
    flex-direction: column;
  }

  .research-showcase .slide-dialog-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 1rem;
    padding: 0.75rem 1rem;
    border-bottom: 1px solid var(--global-divider-color);
  }

  .research-showcase .slide-dialog-header form {
    margin: 0;
  }

  .research-showcase .slide-dialog-header button {
    padding: 0 0.35rem;
    border: 0;
    color: var(--global-text-color);
    background: transparent;
    font-size: 1.8rem;
    line-height: 1;
    cursor: pointer;
  }

  .research-showcase .slide-dialog iframe {
    flex: 1;
    width: 100%;
    border: 0;
  }

  .research-showcase .slide-dialog-link {
    padding: 0.65rem 1rem;
    border-top: 1px solid var(--global-divider-color);
    text-align: right;
  }

  @media (max-width: 767px) {
    .research-showcase .talk-grid {
      grid-template-columns: 1fr;
    }
  }

</style>

<script>
  document.querySelectorAll('.slide-viewer-trigger').forEach((trigger) => {
    trigger.addEventListener('click', () => {
      const dialog = document.getElementById(trigger.dataset.dialog);
      const frame = dialog?.querySelector('iframe');

      if (!dialog || typeof dialog.showModal !== 'function') {
        window.open(trigger.dataset.pdf, '_blank', 'noopener');
        return;
      }

      if (frame && !frame.hasAttribute('src')) frame.src = frame.dataset.src;
      dialog.showModal();
    });
  });

  document.querySelectorAll('.slide-dialog').forEach((dialog) => {
    dialog.addEventListener('click', (event) => {
      if (event.target === dialog) dialog.close();
    });
  });
</script>
