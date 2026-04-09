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
    <p class="project-page-sub">A paint color visualizer built to be iframed into Land of Color.</p>
  </div>
  <img src="/assets/images/PaintDotBanner.png" class="project-page-banner" alt="Paint Dot Generator" style="max-height: 250px; object-fit: contain;">
</section>

<hr>

<section id="project-description">
  <h2>About the Project</h2>
  <p>
    Paint Dot Generator is a web-based paint color visualization tool that lets users browse, 
    search, and preview paint colors in a clean, intuitive interface. Built with vanilla 
    JavaScript, CSS, and HTML, it is designed to be embedded via iframe into the Land of Color platform.
  </p>
  <p>
    The app pulls from a large database of paint color values hosted on AWS, rendering accurate 
    color previews with a focus on performance, usability, and strong visual branding.
  </p>
</section>

<hr>

<section id="project-tech">
  <h2>Tech Breakdown</h2>
  <div class="tech-grid">
    <div class="tech-card">
      <h3>AWS Hosting</h3>
      <p>Application and assets hosted on AWS, ensuring reliable uptime, fast delivery, and scalable infrastructure for the embedded tool.</p>
    </div>
    <div class="tech-card">
      <h3>Large Database Management</h3>
      <p>Manages a large dataset of paint color values including names, hex codes, and vendor data — optimized for fast search and retrieval.</p>
    </div>
    <div class="tech-card">
      <h3>UI / UX Design</h3>
      <p>Clean, minimal interface designed for ease of use — users can search, browse, and preview colors with immediate visual feedback.</p>
    </div>
    <div class="tech-card">
      <h3>Branding</h3>
      <p>Visual identity designed to align with the Land of Color platform — consistent color language, typography, and component styling throughout.</p>
    </div>
    <div class="tech-card">
      <h3>iframe Integration</h3>
      <p>Built specifically to be embedded via iframe into third-party platforms, with responsive layout and clean boundaries for seamless integration.</p>
    </div>
    <div class="tech-card">
      <h3>Vanilla JS / HTML / CSS</h3>
      <p>No frameworks or dependencies — built entirely with vanilla JavaScript, HTML, and CSS for a lightweight, fast-loading experience.</p>
    </div>
  </div>
</section>

<hr>

<section id="project-screenshots">
  <h2>Screenshots</h2>
  <div class="screenshot-gallery">
    <img src="/assets/images/PDG_1.png" alt="Screenshot 1">
    <img src="/assets/images/PDG_2.png" alt="Screenshot 2">
    <img src="/assets/images/PDG_3.png" alt="Screenshot 3">
    <img src="/assets/images/PDG_4.png" alt="Screenshot 4">
    <img src="/assets/images/PDG_5.png" alt="Screenshot 5">
    <img src="/assets/images/PDG_6.png" alt="Screenshot 6">
  </div>
</section>

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
