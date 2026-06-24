---
layout: single
title: "Research"
permalink: /research/
author_profile: true
---

<div class="research-intro">
  <p>I study how galaxies grow and evolve through the movement of gas into, out of and around them. This exchange of matter, known as the baryon cycle, supplies the fuel for star formation and black hole growth, while feedback returns gas and metals to the surrounding environment.</p>

  <p>My research follows this cycle across a range of physical scales. I study gas flowing within galaxies, the extended reservoirs of material in the circumgalactic medium (CGM) and cold neutral hydrogen detected at radio wavelengths. By combining large spectroscopic surveys, detailed observations and cosmological simulations, I aim to understand where galactic gas comes from, how it moves and how it regulates the evolution of galaxies.</p>
</div>

<section class="research-topic research-topic--figure-left">
  <figure class="research-topic__figure">
    <button class="research-topic__image-button" type="button" data-research-image="/files/ExampleSetSeed9.png" data-research-caption="Example absorption profiles used to identify gas flows in galaxy spectra." aria-label="Enlarge example absorption profiles">
      <img src="/files/ExampleSetSeed9.png" alt="Examples of absorption-line profile fits for galaxies with inflowing and outflowing gas" loading="eager">
    </button>
    <figcaption>Example absorption profiles used to identify gas flows in galaxy spectra.</figcaption>
  </figure>

  <div class="research-topic__copy">
    <h2>Gas flows within galaxies</h2>
    <p>Galaxies require a continuing supply of gas to sustain star formation, yet direct observations of accretion remain rare. I investigate inflows and outflows using “down-the-barrel” spectroscopy, in which gas is detected in absorption against a galaxy’s own starlight.</p>

    <p>Using spectra from the Dark Energy Spectroscopic Instrument, I have identified more than 50,000 galaxies with Na I D absorption, including over 10,000 systems consistent with inflowing gas. This represents the first large, systematic observational study of galactic inflows and increases the available sample by more than a factor of 100.</p>

    <p>These inflows span a broad range of velocities and likely arise through several physical channels. Slow inflows may trace motion within galactic discs or material returning through galactic fountains, while the fastest systems are more consistent with satellite accretion and galaxy interactions. Studying these flows across a large and diverse population provides new insight into how accretion, feedback and environment shape galaxy growth.</p>
  </div>
</section>

<section class="research-topic research-topic--figure-right">
  <div class="research-topic__copy">
    <h2>Origins of gas in the circumgalactic medium</h2>
    <p>The circumgalactic medium is the extended atmosphere of gas surrounding a galaxy. It contains material drawn from the wider cosmic environment, gas expelled through feedback and matter associated with satellite galaxies.</p>

    <p>I investigate the origins of cool CGM gas by combining absorption-line observations with cosmological simulations. My observational work uses surveys such as MUSE-ALMA Haloes to connect absorbing material with nearby galaxies and their environments. I also use the TNG50 simulation to trace the histories and motions of gas that would be observable in absorption.</p>

    <p>This research challenges the simple picture in which accretion occurs mainly along a galaxy’s major axis and outflows dominate along its minor axis. Instead, the cool CGM appears to be shaped by a mixture of accretion, feedback, satellite galaxies and slowly moving material within the halo.</p>
  </div>

  <figure class="research-topic__figure">
    <button class="research-topic__image-button" type="button" data-research-image="/files/TNGMandatory.png" data-research-caption="TNG50 sightlines tracing the column density and origins of cool CGM gas." aria-label="Enlarge TNG50 circumgalactic gas figure">
      <img src="/files/TNGMandatory.png" alt="TNG50 maps showing neutral hydrogen and the gravitational and flow origins of circumgalactic gas" loading="lazy">
    </button>
    <figcaption>TNG50 sightlines tracing the column density and origins of cool CGM gas.</figcaption>
  </figure>
</section>

<section class="research-topic research-topic--wide">
  <div class="research-topic__copy">
    <h2>Neutral hydrogen through 21-cm absorption</h2>
    <p>The 21-cm transition of neutral hydrogen provides a sensitive probe of cold atomic gas, from which molecular clouds and stars can eventually form. When this material lies in front of a bright radio source, it can be detected in absorption even at distances where 21-cm emission is difficult to observe.</p>

    <p>I am involved in the First Large Absorption Survey in H I, or FLASH, conducted with the Australian Square Kilometre Array Pathfinder. FLASH searches for redshifted 21-cm absorption across a large area of the sky, providing a statistical view of cold neutral gas at intermediate redshifts.</p>

    <p>My work focuses on identifying the galaxies and larger environments associated with these absorbers using optical imaging and spectroscopy. I also contribute to evaluating candidate systems and identifying instrumental artefacts, helping to produce a reliable catalogue for studies of the evolution of cold gas.</p>
  </div>

  <figure class="research-topic__figure research-topic__figure--wide">
    <button class="research-topic__image-button" type="button" data-research-image="/files/PPXF_fig4.png" data-research-caption="Example spectral fits used to characterise galaxies associated with FLASH absorbers." aria-label="Enlarge FLASH spectral fitting figure">
      <img src="/files/PPXF_fig4.png" alt="Three optical spectra with fitted models used to characterise FLASH absorber host galaxies" loading="lazy">
    </button>
    <figcaption>Example spectral fits used to characterise galaxies associated with FLASH absorbers.</figcaption>
  </figure>
</section>

<dialog class="research-lightbox" id="research-lightbox" aria-label="Enlarged research figure" aria-describedby="research-lightbox-caption">
  <button class="research-lightbox__close" type="button" aria-label="Close enlarged figure">
    <i class="fas fa-xmark" aria-hidden="true"></i>
  </button>
  <img class="research-lightbox__image" src="" alt="">
  <p class="research-lightbox__caption" id="research-lightbox-caption"></p>
</dialog>

<script>
  (() => {
    const dialog = document.getElementById('research-lightbox');
    const enlargedImage = dialog.querySelector('.research-lightbox__image');
    const caption = dialog.querySelector('.research-lightbox__caption');
    const closeButton = dialog.querySelector('.research-lightbox__close');

    document.querySelectorAll('[data-research-image]').forEach((button) => {
      button.addEventListener('click', () => {
        const thumbnail = button.querySelector('img');
        enlargedImage.src = button.dataset.researchImage;
        enlargedImage.alt = thumbnail.alt;
        caption.textContent = button.dataset.researchCaption;
        dialog.showModal();
      });
    });

    closeButton.addEventListener('click', () => dialog.close());
    dialog.addEventListener('click', (event) => {
      if (event.target === dialog) dialog.close();
    });
  })();
</script>
