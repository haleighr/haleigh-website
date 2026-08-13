<!--My epic awesome sauce website-->

<!--This script is for the projects section-->
<script>
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
</script>

<svelte:head>
  <title>Haleigh Renfroe | Personal Website</title>
  <meta
    name="description"
    content="My epic website!"
  />
</svelte:head>

<main class="page-shell">
  <section class="intro" aria-labelledby="intro-title">
    <p class="eyebrow">Personal Portfolio</p>
    <h1 id="intro-title">Haleigh Renfroe</h1>
    <p class="summary">
      Hi! I'm Haleigh. I'm a software engineer who likes making cool things, and learning about cool things.
    </p>
    <div class="actions" aria-label="Primary links">
      <a href="#projects">View Projects</a>
      <a href="#contact">Contact</a>
    </div>
  </section>

  <section class="section" aria-labelledby="about-title">
    <p class="section-label">About</p>
    <h2 id="about-title">A little about me</h2>
    <p>
      I graduated from Morehead State University in 2026 with a degree in Computer Science. I currently work now at MSU as a Space Systems Software Engineer.
      Besides that, I like music (I play the drums and bass), spending time with my family and my cat Tina, and playing video games with my friends!
    </p>
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
    <p>
      
    </p>
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

  .actions a {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    min-height: 44px;
    padding: 0 18px;
    border: 1px solid #85d7df;
    color: #ffffff;
    text-decoration: none;
    font-weight: 700;
  }

  .actions a:first-child {
    background: #85d7df;
    color: #06293d;
  }

  .section {
    padding: 72px 0;
    border-top: 1px solid rgba(133, 215, 223, 0.24);
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

  @media (max-width: 760px) {
    .page-shell {
      padding: 48px 20px;
    }

    .intro {
      min-height: 64vh;
    }

    .project-list {
      grid-template-columns: 1fr;
    }
  }
</style>
