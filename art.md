---
layout: default
title: Art
---

# Art

<div class="art-piece">
  <div class="art-piece-description">
    <h2>Click!</h2>
    <p>Shot using Stop Motion Studio<br>
    Audio by Eireann Coelho<br>
    Display edited by Eireann Coelho<br>
    Click the image to watch the video!</p>
  </div>
  <a href="https://youtu.be/CRl5QiZaHEw" target="_blank" rel="noopener" class="art-piece-visual">
    <img src="{{ '/assets/art/click.png' | relative_url }}" alt="Click! - Stop motion piece by Eireann Coelho">
  </a>
</div>

<div class="art-piece">
  <div class="art-piece-description">
    <h2>Dynamic</h2>
    <p>Created in Processing 4<br>
    Click the image to watch the video!</p>
  </div>
  <a href="https://youtube.com/shorts/GiD1KZ-zUpg?feature=share" target="_blank" rel="noopener" class="art-piece-visual">
    <img src="{{ '/assets/art/dynamic.png' | relative_url }}" alt="Dynamic - Processing 4 piece by Eireann Coelho">
  </a>
</div>

<div class="art-piece">
  <div class="art-piece-description">
    <h2>Stamp</h2>
    <p>Created in Processing, this code takes an image and maps the intensity of the color of a pixel to the stamp shape. The darker the color, the more petals on the flower.</p>
  </div>
  <button type="button" class="art-piece-visual art-piece-lightbox" data-modal-src="{{ '/assets/art/stamp.png' | relative_url }}" aria-label="View Stamp larger">
    <img src="{{ '/assets/art/stamp.png' | relative_url }}" alt="Stamp by Eireann Coelho">
  </button>
</div>

<div class="art-piece">
  <div class="art-piece-description">
    <h2></h2>
    <p>Here is a collection of three words described visually through simple vectors. Created in Adobe Illustrator.</p>
  </div>
  <button type="button" class="art-piece-visual art-piece-lightbox" data-modal-src="{{ '/assets/art/words.png' | relative_url }}" aria-label="View Words larger">
    <img src="{{ '/assets/art/words.png' | relative_url }}" alt="Words - vector art by Eireann Coelho">
  </button>
</div>

<div id="art-lightbox" class="art-lightbox" role="dialog" aria-modal="true" aria-label="Enlarged image view" hidden>
  <button type="button" class="art-lightbox-close" aria-label="Close">×</button>
  <div class="art-lightbox-content">
    <img src="" alt="" id="art-lightbox-img">
  </div>
</div>

<script>
(function() {
  var lightbox = document.getElementById('art-lightbox');
  var lightboxImg = document.getElementById('art-lightbox-img');
  var closeBtn = lightbox.querySelector('.art-lightbox-close');
  var triggers = document.querySelectorAll('.art-piece-lightbox');

  function openLightbox(src, alt) {
    lightboxImg.src = src;
    lightboxImg.alt = alt;
    lightbox.hidden = false;
    document.body.style.overflow = 'hidden';
  }

  function closeLightbox() {
    lightbox.hidden = true;
    document.body.style.overflow = '';
  }

  triggers.forEach(function(btn) {
    btn.addEventListener('click', function() {
      var src = this.getAttribute('data-modal-src');
      var alt = this.querySelector('img').alt;
      openLightbox(src, alt);
    });
  });

  closeBtn.addEventListener('click', closeLightbox);

  lightbox.addEventListener('click', function(e) {
    if (e.target === lightbox) closeLightbox();
  });

  document.addEventListener('keydown', function(e) {
    if (e.key === 'Escape') closeLightbox();
  });
})();
</script>
