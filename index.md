---
layout: default
title: "Nic Sawaya"
---

<section id="about">
  <div class="hero">
    <img src="assets/images/profile.jpg" alt="Nic Sawaya" class="hero-photo">
    <h1 class="hero-name">Nic Sawaya</h1>
    <p class="hero-tagline">Game Developer · FPS Systems · Unreal Engine</p>
    <p class="hero-bio">
      I'm a game developer focused on building atmospheric, systems‑driven experiences
      with clean mechanics and strong visual identity. My work blends retro‑futuristic
      aesthetics, modular gameplay systems, and tight moment‑to‑moment feel.
    </p>
   <!-- <div class="hero-stats">
      <div class="stat">
        <span class="stat-number">2+</span>
        <span class="stat-label">Years Experience</span>
      </div>
      <div class="stat">
        <span class="stat-number">3+</span>
        <span class="stat-label">Projects Shipped</span>
      </div>
      <div class="stat">
        <span class="stat-number">2</span>
        <span class="stat-label">Engines Used</span>
      </div>
   </div> -->
    <div class="hero-btns">
      <a href="#projects" class="btn-primary">View Projects</a>
      <a href="#contact" class="btn-secondary">Contact</a>
      <a href="#" class="btn-secondary">Resume</a>
    </div>
  </div>
</section>

<hr>

<section id="projects">
  <h2>Projects</h2>
  <p class="section-sub">A collection of games, apps, and prototypes I've built and iterated on.</p>

  <div class="filter-tabs">
    <button class="filter-btn active" data-filter="game">Games</button>
    <button class="filter-btn" data-filter="app">Apps</button>
    <button class="filter-btn" data-filter="prototype">Prototypes</button>
  </div>

  <div class="project-list">

    <!-- ORBIT PROTOCOL -->
    <a class="project-row" data-category="game" href="/projects/orbit-protocol">
      <div class="project-row-left">
        <img src="assets/images/OrbitLogoV1.png" class="project-main-shot" alt="Orbit Protocol">
        <div class="project-tags-top">
          <span class="tag">Unreal Engine</span>
          <span class="tag">FPS</span>
          <span class="tag">Roguelite</span>
          <span class="tag">C++</span>
        </div>
        <div class="project-title-bottom">
          <h3>Orbit Protocol</h3>
        </div>
      </div>
      <div class="project-row-right">
        <img src="assets/images/orbit-screen1.png" alt="Screenshot 1">
        <img src="assets/images/orbit-screen2.png" alt="Screenshot 2">
        <img src="assets/images/orbit-screen3.png" alt="Screenshot 3">
      </div>
    </a>

    <!-- PLACEHOLDER GAME -->
    <a class="project-row" data-category="game" href="#">
      <div class="project-row-left">
        <img src="https://placehold.co/320x240/111/333?text=Coming+Soon" class="project-main-shot" alt="Project Title">
        <div class="project-tags-top">
          <span class="tag">Unreal Engine</span>
          <span class="tag">Coming Soon</span>
        </div>
        <div class="project-title-bottom">
          <h3>Project Title</h3>
        </div>
      </div>
      <div class="project-row-right">
        <img src="https://placehold.co/200x80/111/333?text=Screenshot" alt="Screenshot 1">
        <img src="https://placehold.co/200x80/111/333?text=Screenshot" alt="Screenshot 2">
        <img src="https://placehold.co/200x80/111/333?text=Screenshot" alt="Screenshot 3">
      </div>
    </a>

    <!-- PLACEHOLDER APP -->
    <a class="project-row" data-category="app" href="#">
      <div class="project-row-left">
        <img src="https://placehold.co/320x240/111/333?text=Coming+Soon" class="project-main-shot" alt="App Title">
        <div class="project-tags-top">
          <span class="tag">Coming Soon</span>
        </div>
        <div class="project-title-bottom">
          <h3>App Title</h3>
        </div>
      </div>
      <div class="project-row-right">
        <img src="https://placehold.co/200x80/111/333?text=Screenshot" alt="Screenshot 1">
        <img src="https://placehold.co/200x80/111/333?text=Screenshot" alt="Screenshot 2">
        <img src="https://placehold.co/200x80/111/333?text=Screenshot" alt="Screenshot 3">
      </div>
    </a>

  </div>
</section>

<script>
  const filterBtns = document.querySelectorAll('.filter-btn');
  const rows = document.querySelectorAll('.project-row');

  rows.forEach(row => {
    if (row.dataset.category !== 'game') {
      row.classList.add('hidden');
    }
  });

  filterBtns.forEach(btn => {
    btn.addEventListener('click', () => {
      filterBtns.forEach(b => b.classList.remove('active'));
      btn.classList.add('active');
      const filter = btn.dataset.filter;
      rows.forEach(row => {
        if (row.dataset.category === filter) {
          row.classList.remove('hidden');
        } else {
          row.classList.add('hidden');
        }
      });
    });
  });
</script>

<hr>

<section id="skills">
  <h2>Skills</h2>
  <p class="section-sub">Tools, technologies, and areas I work in.</p>
  <div class="skills-grid">
    <div class="skill-item">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/cplusplus/cplusplus-original.svg" alt="C++">
    </div>
    <div class="skill-item">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/unrealengine/unrealengine-original.svg" alt="Unreal Engine">
    </div>
    <div class="skill-item">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/qt/qt-original.svg" alt="Qt Creator">
    </div>
    <div class="skill-item">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" alt="Git">
    </div>
    <div class="skill-item">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" alt="CSS">
    </div>
    <div class="skill-item">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/azuresqldatabase/azuresqldatabase-original.svg" alt="SQL">
    </div>
    <div class="skill-item">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/premierepro/premierepro-plain.svg" alt="Premiere Pro">
    </div>
    <div class="skill-item">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/visualstudio/visualstudio-plain.svg" alt="Visual Studio">
    </div>
  </div>
</section>

<hr>

<section id="contact">
  <h2>Contact</h2>
  <p><strong>Email:</strong> your-email-here</p>
  <p><strong>GitHub:</strong> <a href="https://github.com/Nic-devv">github.com/Nic-devv</a></p>
</section>
