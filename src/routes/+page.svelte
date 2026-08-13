<!--My epic awesome sauce website-->


<script>
  import documentIcon from '$lib/assets/document-layout-right-svgrepo-com.svg';
  import emailIcon from '$lib/assets/email-1-svgrepo-com.svg';
  import githubIcon from '$lib/assets/github-142-svgrepo-com.svg';
  import linkedinIcon from '$lib/assets/linkedin-svgrepo-com.svg';
  import resumeHref from '$lib/assets/Haleigh_Renfroe_Resume_August_2026.pdf';
  import tinaPhoto from '$lib/assets/loving_tina.jpg';

  const projects = [
    {
      title: 'Project One',
      description: 'blah'
    },
    {
      title: 'Project Two',
      description: 'ahhhh'
    },
    {
      title: 'Project Three',
      description: 'idek'
    }
  ];

  const contactLinks = [
    {
      label: 'GitHub',
      href: 'https://github.com/your-username',
      icon: githubIcon
    },
    {
      label: 'LinkedIn',
      href: 'https://www.linkedin.com/in/your-username',
      icon: linkedinIcon
    },
    {
      label: 'Email',
      href: 'mailto:you@example.com',
      icon: emailIcon
    }
  ];
</script>

<svelte:head>
  <title>Haleigh Renfroe | Personal Website</title>
  <meta
    name="description"
    content="My epic website!"
  />
</svelte:head>

<header class="site-header">
  <a class="site-name" href="#intro">Haleigh Renfroe</a>
  <nav aria-label="Main navigation">
    <a href="#about">About</a>
    <a href="#projects">Projects</a>
    <a href={resumeHref} target="_blank" rel="noreferrer">Resume</a>
    <a href="#contact">Contact</a>
  </nav>
</header>

<main class="page-shell">
  <section class="intro" id="intro" aria-labelledby="intro-title">
    <p class="eyebrow">Personal Portfolio</p>
    <h1 id="intro-title">Haleigh Renfroe</h1>
    <p class="summary">
      Hi! I'm Haleigh. I'm a software engineer, and I think programming is really cool! :)
    </p>
    <div class="actions" aria-label="Primary links">
      <a href="#projects">View Projects</a>
      <a href={resumeHref} target="_blank" rel="noreferrer">Resume</a>
      <a href="#contact">Contact</a>
    </div>
  </section>

  <section class="section" id="about" aria-labelledby="about-title">
    <div class="about-layout">
      <div>
        <p class="section-label">About</p>
        <h2 id="about-title">A little about me</h2>
        <p>
          I graduated from Morehead State University in 2026 with a degree in Computer Science. I currently work now at MSU as a Space Systems Software Engineer.
          Besides that, I like music (I play the drums and bass), spending time with my family and my cat Tina, and playing video games with my friends!
        </p>
      </div>

      <figure class="tina-photo">
        <img src={tinaPhoto} alt="Tina the cat" />
        <figcaption>Tina</figcaption>
      </figure>
    </div>
  </section>

  <section class="section" id="projects" aria-labelledby="projects-title">
    <p class="section-label">Projects</p>
    <h2 id="projects-title">Cool Stuff I've Worked On</h2>
    <div class="project-list">
      {#each projects as project}
        <article class="project-card">
          <h3>{project.title}</h3>
          <p>{project.description}</p>
        </article>
      {/each}
    </div>
  </section>

  <section class="section contact" id="contact" aria-labelledby="contact-title">
    <p class="section-label">Contact</p>
    <h2 id="contact-title">If you wanna chat, here's where to find me!</h2>
    <div class="contact-links" aria-label="Contact links">
      {#each contactLinks as link}
        <a href={link.href} aria-label={link.label}>
          <img src={link.icon} alt="" aria-hidden="true" />
          <span>{link.label}</span>
        </a>
      {/each}
      <a href={resumeHref} target="_blank" rel="noreferrer" aria-label="Resume">
        <img src={documentIcon} alt="" aria-hidden="true" />
        <span>Resume</span>
      </a>
    </div>
  </section>
</main>

<style>
  :global(body) {
    margin: 0;
    font-family:
      Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
    color: #edf7f8;
    background: #06293d;
  }

  :global(*) {
    box-sizing: border-box;
  }

  :global(html) {
    scroll-behavior: smooth;
  }

  .site-header {
    position: sticky;
    top: 0;
    z-index: 10;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 20px;
    width: min(100%, 960px);
    margin: 0 auto;
    padding: 18px 24px;
    background: rgba(6, 41, 61, 0.92);
    backdrop-filter: blur(14px);
  }

  .site-header a {
    color: #edf7f8;
    text-decoration: none;
    transition:
      color 180ms ease,
      background 180ms ease,
      border-color 180ms ease,
      transform 180ms ease;
  }

  .site-name {
    font-weight: 800;
  }

  nav {
    display: flex;
    flex-wrap: wrap;
    justify-content: flex-end;
    gap: 16px;
  }

  nav a {
    color: #c6dce2;
    font-size: 0.95rem;
    font-weight: 700;
  }

  nav a:hover,
  .site-name:hover {
    color: #85d7df;
  }

  .page-shell {
    width: min(100%, 960px);
    margin: 0 auto;
    padding: 72px 24px;
  }

  .intro {
    min-height: 70vh;
    display: grid;
    align-content: center;
    gap: 20px;
  }

  .eyebrow,
  .section-label {
    margin: 0;
    color: #85d7df;
    font-size: 0.78rem;
    font-weight: 700;
    letter-spacing: 0;
    text-transform: uppercase;
  }

  h1,
  h2,
  h3,
  p {
    margin-top: 0;
  }

  h1 {
    max-width: 760px;
    margin-bottom: 0;
    color: #ffffff;
    font-size: clamp(3.25rem, 13vw, 7rem);
    line-height: 0.95;
  }

  h2 {
    margin-bottom: 16px;
    color: #ffffff;
    font-size: 2rem;
    line-height: 1.15;
  }

  h3 {
    margin-bottom: 10px;
    color: #ffffff;
    font-size: 1.1rem;
  }

  p {
    max-width: 680px;
    color: #c6dce2;
    font-size: 1rem;
    line-height: 1.7;
  }

  .summary {
    max-width: 680px;
    color: #d9ecef;
    font-size: 1.25rem;
  }

  .actions {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
    margin-top: 8px;
  }

  .actions a,
  .contact-links a {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    min-height: 48px;
    padding: 0 16px;
    border: 1px solid rgba(133, 215, 223, 0.34);
    color: #edf7f8;
    background: rgba(255, 255, 255, 0.04);
    font-weight: 800;
    text-decoration: none;
    transition:
      color 180ms ease,
      background 180ms ease,
      border-color 180ms ease,
      transform 180ms ease;
  }

  .actions a:hover,
  .actions a:focus-visible,
  .contact-links a:hover,
  .contact-links a:focus-visible {
    border-color: #85d7df;
    background: #85d7df;
    color: #06293d;
    transform: translateY(-2px);
  }

  .section {
    scroll-margin-top: 84px;
    padding: 72px 0;
    border-top: 1px solid rgba(133, 215, 223, 0.24);
  }

  .about-layout {
    display: grid;
    grid-template-columns: minmax(0, 1fr) 220px;
    gap: 40px;
    align-items: center;
  }

  .tina-photo {
    margin: 0;
  }

  .tina-photo img {
    display: block;
    width: 100%;
    aspect-ratio: 1;
    object-fit: cover;
    border: 2px solid #85d7df;
    border-radius: 50%;
    box-shadow: 0 20px 50px rgba(0, 0, 0, 0.24);
    transition: transform 1000ms;
  }

  .tina-photo:hover img {
    transform: rotate(360deg);
  }

  .tina-photo figcaption {
    margin-top: 12px;
    color: #85d7df;
    font-size: 0.9rem;
    font-weight: 700;
    text-align: center;
  }

  .project-list {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 16px;
  }

  .project-card {
    min-height: 180px;
    padding: 22px;
    border: 1px solid rgba(133, 215, 223, 0.28);
    background: rgba(255, 255, 255, 0.04);
  }

  .project-card p {
    margin-bottom: 0;
    font-size: 0.95rem;
  }

  .contact {
    padding-bottom: 0;
  }

  .contact-links {
    display: flex;
    flex-wrap: wrap;
    gap: 14px;
  }

  .contact-links a {
    gap: 10px;
  }

  .contact-links img {
    width: 22px;
    height: 22px;
    object-fit: contain;
    flex: 0 0 auto;
  }

</style>
