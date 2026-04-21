---
layout: default
title: "Paint Dot Generator"
---

<section id="project-hero">
  <div class="project-page-header">
    <a href="/" class="back-btn">← Back</a>
    <div class="project-page-tags">
      <span class="tag">Web App</span>
      <span class="tag">JavaScript</span>
      <span class="tag">CSS</span>
      <span class="tag">HTML</span>
    </div>
    <h1 class="project-page-title">Paint Dot Generator</h1>
    <p class="project-page-sub">A paint color visualizer and mood board tool built for Land of Color.</p>
  </div>
  <img src="/assets/images/PaintDotBanner.png" class="project-page-banner" alt="Paint Dot Generator" style="max-height: 250px; object-fit: contain;">
</section>

<hr>

<section id="project-description">
  <h2>About the Project</h2>
  <p>
    Paint Dot Generator is a web-based paint color visualization tool that lets users browse, 
    search, and preview paint colors in a clean, intuitive interface. Built with vanilla 
    JavaScript, CSS, and HTML, it is designed to be embedded into the Land of Color platform.
  </p>
  <p>
    The tool also includes a lightweight Mood Board editor, allowing users to drag, arrange, 
    and experiment with paint blobs and reference images on a freeform canvas.
  </p>
</section>

<hr>


<section id="mood-board">
  <h2>Mood Board Editor</h2>
  <p>
    A built‑in mini image editor that lets users drag, arrange, and experiment with paint colors 
    on a freeform canvas. Designed for quick palette exploration and visual inspiration.
  </p>

  <div class="screenshot-gallery">
    <img src="/assets/images/paintdot/pdgss1.png" alt="Mood Board Screenshot 1">
    <img src="/assets/images/paintdot/pdgss2.png" alt="Mood Board Screenshot 2">
    <img src="/assets/images/paintdot/pdgss3.png" alt="Mood Board Screenshot 3">
  </div>
</section>

<hr>


<section id="color-picker">
  <h2>Color Picker & Blob Generator</h2>
  <p>
    The main interface for browsing, searching, and previewing paint colors. Users can generate 
    branded paint blobs, explore color attributes, and view accurate swatches in real time.
  </p>

  <div class="screenshot-gallery">
    <img src="/assets/images/paintdot/pdgss4.png" alt="Color Picker Screenshot 1">
    <img src="/assets/images/paintdot/pdgss5.png" alt="Color Picker Screenshot 2">
    <img src="/assets/images/paintdot/pdgss6.png" alt="Color Picker Screenshot 3">
  </div>
</section>

<hr>


<div class="lightbox-overlay" id="lightbox">
  <button class="lightbox-close" id="lightbox-close">✕</button>
  <button class="lightbox-prev" id="lightbox-prev">‹</button>
  <img class="lightbox-img" id="lightbox-img" src="" alt="">
  <button class="lightbox-next" id="lightbox-next">›</button>
</div>

<script>
  const gallery = document.querySelectorAll('.screenshot-gallery img');
  const lightbox = document.getElementById('lightbox');
  const lightboxImg = document.getElementById('lightbox-img');
  let current = 0;

  function openLightbox(index) {
    current = index;
    lightboxImg.src = gallery[current].src;
    lightbox.classList.add('active');
  }

  function closeLightbox() {
    lightbox.classList.remove('active');
  }

  function showPrev() {
    current = (current - 1 + gallery.length) % gallery.length;
    lightboxImg.src = gallery[current].src;
  }

  function showNext() {
    current = (current + 1) % gallery.length;
    lightboxImg.src = gallery[current].src;
  }

  gallery.forEach((img, i) => {
    img.addEventListener('click', () => openLightbox(i));
  });

  document.getElementById('lightbox-close').addEventListener('click', closeLightbox);
  document.getElementById('lightbox-prev').addEventListener('click', showPrev);
  document.getElementById('lightbox-next').addEventListener('click', showNext);

  lightbox.addEventListener('click', (e) => {
    if (e.target === lightbox) closeLightbox();
  });

  document.addEventListener('keydown', (e) => {
    if (!lightbox.classList.contains('active')) return;
    if (e.key === 'ArrowLeft') showPrev();
    if (e.key === 'ArrowRight') showNext();
    if (e.key === 'Escape') closeLightbox();
  });
</script>
