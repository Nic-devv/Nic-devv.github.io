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
   <!-- </p>
     <div class="hero-stats">
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
      </div> -->
    </div>
    <div class="hero-btns">
      <a href="#projects" class="btn-primary">View Projects</a>
      <a href="#contact" class="btn-secondary">Contact</a>
      <a href="#" class="btn-secondary" id="resume-btn">Resume</a>
    </div>
  </div>
</section>

<hr>

<section id="projects">
  <h2>Projects</h2>
  <p class="section-sub">A collection of games and prototypes I've built and iterated on.</p>
  <div class="filter-tabs">
    <button class="filter-btn active" data-filter="all">All</button>
    <button class="filter-btn" data-filter="game">Games</button>
    <button class="filter-btn" data-filter="prototype">Prototypes</button>
  </div>
  <div class="project-grid">
    <div class="project-card" data-category="game">
      <img src="assets/images/OrbitLogoV1.png" class="project-thumb" alt="Orbit Protocol">
      <div class="project-info">
        <div class="project-tags">
          <span class="tag">Unreal Engine</span>
          <span class="tag">FPS</span>
          <span class="tag">Roguelite</span>
          <span class="tag">C++</span>
        </div>
        <h3>Orbit Protocol</h3>
        <a class="project-btn" href="/projects/orbit-protocol">View Project</a>
      </div>
    </div>
  </div>
</section>

<script>
  const filterBtns = document.querySelectorAll('.filter-btn');
  const cards = document.querySelectorAll('.project-card');
  filterBtns.forEach(btn => {
    btn.addEventListener('click', () => {
      filterBtns.forEach(b => b.classList.remove('active'));
      btn.classList.add('active');
      const filter = btn.dataset.filter;
      cards.forEach(card => {
        if (filter === 'all' || card.dataset.category === filter) {
          card.classList.remove('hidden');
        } else {
          card.classList.add('hidden');
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
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" alt="CSS">
     
    </div>

    <div class="skill-item">
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/azuresqldatabase/azuresqldatabase-original.svg" /> 
    </div>

    <div class="skill-item">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/qt/qt-original.svg" alt="Qt Creator">
     
    </div>

    <div class="skill-item">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/unrealengine/unrealengine-original.svg" alt="Unreal Engine">

    </div>

    <div class="skill-item">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" alt="Git">      
    </div>
    <div class="skill-item">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/premierepro/premierepro-plain.svg" alt="Premiere Pro">
  
</div>

<div class="skill-item">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/visualstudio/visualstudio-plain.svg" alt="Visual Studio">
  
</div>

  </div>
</section>

<section id="contact">
  <h2>Contact</h2>
  <p><strong>Email:</strong> your-email-here</p>
  <p><strong>GitHub:</strong> <a href="https://github.com/Nic-devv">github.com/Nic-devv</a></p>
</section>
