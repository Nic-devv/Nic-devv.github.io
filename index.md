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
      I'm a game designer and programmer focused on building systems driven experiences
      with clean mechanics and satisfying loops. My work 
      centers around modular gameplay systems, and building organized, purposeful environments.
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
      <a href="/assets/ResumeV2.pdf" class="btn-secondary" target="_blank">Resume</a>
    </div>
  </div>
</section>

<hr>

<section id="projects">
  <h2>Projects</h2>
  <p class="section-sub">A collection of games and prototypes I've built and iterated on.</p>

  <div class="filter-tabs">
    <button class="filter-btn active" data-filter="game">Games</button>
    <button class="filter-btn" data-filter="prototype">Prototypes</button>
  </div>

  <div class="project-grid">

    <a class="project-card" data-category="game" href="/projects/orbit-protocol">
      <img src="assets/images/OrbitLogoV1.png" class="project-thumb" alt="Orbit Protocol">
      <div class="project-tags-top">
        <span class="tag">Unreal Engine</span>
        <span class="tag">FPS</span>
        <span class="tag">Roguelite</span>
        <span class="tag">C++</span>
      </div>
      <div class="project-title-bottom">
        <h3>Orbit Protocol</h3>
      </div>
    </a>

    <a class="project-card" data-category="game" href="/projects/velocity-loop">
      <img src="/assets/images/VelocityLoopBanner.png" class="project-thumb" alt="Velocity Loop">
      <div class="project-tags-top">
        <span class="tag">Unreal Engine</span>
        <span class="tag">3rd Person</span>
        <span class="tag">Platformer</span>
      </div>
      <div class="project-title-bottom">
        <h3>Velocity Loop</h3>
      </div>
    </a>

  </div>
</section>

<script>
  const filterBtns = document.querySelectorAll('.filter-btn');
  const cards = document.querySelectorAll('.project-card');

  cards.forEach(card => {
    if (card.dataset.category !== 'game') {
      card.classList.add('hidden');
    }
  });

  filterBtns.forEach(btn => {
    btn.addEventListener('click', () => {
      filterBtns.forEach(b => b.classList.remove('active'));
      btn.classList.add('active');
      const filter = btn.dataset.filter;
      cards.forEach(card => {
        if (card.dataset.category === filter) {
          card.classList.remove('hidden');
        } else {
          card.classList.add('hidden');
        }
      });
    });
  });
</script>

<hr>

<section id="apps">
  <h2>Apps/Tools</h2>
  <p class="section-sub">Software and tools I've designed and built.</p>


  <a class="project-card" href="/projects/paint-dot-generator">
  <img src="/assets/images/PaintDotBanner.png" class="project-thumb" alt="Paint Dot Generator">
  <div class="project-tags-top">
    <span class="tag">Web App</span>
    <span class="tag">JavaScript</span>
    <span class="tag">CSS</span>
    <span class="tag">HTML</span>
  </div>
  <div class="project-title-bottom">
    <h3>Paint Dot Generator</h3>
  </div>
</a>

 <div class="project-grid">
  <a class="project-card" href="/projects/chroma-bench">
    <img src="/assets/images/ChromaBenchBannerV1.png" class="project-thumb" alt="Chroma Bench" style="object-fit: contain; background: #111;">
    <div class="project-tags-top">
      <span class="tag">Color Visualization</span>
      <span class="tag">Color Science UI</span>
      <span class="tag">NDA‑Compliant</span>
    </div>
    <div class="project-title-bottom" style="background: rgba(0,0,0,0.85); padding: 0.25rem 1rem;">
      <h3>Chroma Bench(Beta)</h3>
    </div>
  </a>
</div>
</section>

<hr>

<section id="skills">
  <h2>Skills</h2>
  <p class="section-sub">Tools, technologies, and areas I work in.</p>
  <div class="skills-grid">
    <div class="skill-item">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/cplusplus/cplusplus-original.svg" alt="C++">
    </div>
    <div class="skill-item">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/unrealengine/unrealengine-original.svg" alt="Unreal Engine">
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
    <div class="skill-item">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" alt="HTML5">
    </div>
  </div>
</section>

<hr>

<section id="contact">
  <h2>Contact</h2>
  <p><strong>Email:</strong> your-email-here</p>
  <p><strong>GitHub:</strong> <a href="https://github.com/Nic-devv">github.com/Nic-devv</a></p>
</section>
