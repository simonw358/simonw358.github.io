---
layout: single
title: "Other Interests"
permalink: /other-interests/
author_profile: true
---

## Cooking

Away from astronomy, I enjoy cooking and experimenting with new dishes. Here are a few things to come out of my kitchen recently.

<div class="food-gallery">
  <button class="food-gallery__item" type="button" data-food-image="/images/food/IMG_0688_edited.png" aria-label="Enlarge fried rice dish">
    <img src="/images/food/IMG_0688_edited.png" alt="Fried rice with vegetables, coriander, and chilli crisp in a blue bowl" loading="eager">
  </button>
  <button class="food-gallery__item" type="button" data-food-image="/images/food/IMG_0675_edited.png" aria-label="Enlarge noodle and tofu dish">
    <img src="/images/food/IMG_0675_edited.png" alt="Noodles with tofu, spring onions, and a crisp garnish" loading="lazy">
  </button>
  <button class="food-gallery__item" type="button" data-food-image="/images/food/IMG_0653_full-plate.png" aria-label="Enlarge glazed vegetable dish">
    <img src="/images/food/IMG_0653_full-plate.png" alt="Glazed vegetable rounds with herbs on a floral plate" loading="lazy">
  </button>
  <button class="food-gallery__item" type="button" data-food-image="/images/food/IMG_0673_edited.png" aria-label="Enlarge charred cabbage dish">
    <img src="/images/food/IMG_0673_edited.png" alt="Charred cabbage wedges with a green herb dressing" loading="lazy">
  </button>
  <button class="food-gallery__item" type="button" data-food-image="/images/food/IMG_0644_edited.png" aria-label="Enlarge sesame noodle dish">
    <img src="/images/food/IMG_0644_edited.png" alt="Noodles with a creamy sesame sauce, coriander, spring onion, and chilli oil" loading="lazy">
  </button>
</div>

<dialog class="food-lightbox" id="food-lightbox" aria-label="Enlarged food photograph">
  <button class="food-lightbox__close" type="button" aria-label="Close enlarged image">
    <i class="fas fa-xmark" aria-hidden="true"></i>
  </button>
  <img class="food-lightbox__image" src="" alt="">
</dialog>

<script>
  (() => {
    const dialog = document.getElementById('food-lightbox');
    const enlargedImage = dialog.querySelector('.food-lightbox__image');
    const closeButton = dialog.querySelector('.food-lightbox__close');

    document.querySelectorAll('[data-food-image]').forEach((button) => {
      button.addEventListener('click', () => {
        const thumbnail = button.querySelector('img');
        enlargedImage.src = button.dataset.foodImage;
        enlargedImage.alt = thumbnail.alt;
        dialog.showModal();
      });
    });

    closeButton.addEventListener('click', () => dialog.close());
    dialog.addEventListener('click', (event) => {
      if (event.target === dialog) dialog.close();
    });
  })();
</script>
