<script>
  import documentIcon from '$lib/assets/document-layout-right-svgrepo-com.svg';
  import emailIcon from '$lib/assets/email-1-svgrepo-com.svg';
  import githubIcon from '$lib/assets/github-142-svgrepo-com.svg';
  import linkedinIcon from '$lib/assets/linkedin-svgrepo-com.svg';
  import resumeHref from '$lib/assets/Haleigh_Renfroe_Resume_August_2026.pdf';
  import tinaPhoto from '$lib/assets/loving_tina.jpg';

  const projects = [
    { title: 'Project One', description: 'More details coming soon...', icon: '💾', tag: 'software' },
    { title: 'Project Two', description: 'Currently under construction!', icon: '🛰️', tag: 'space stuff' },
    { title: 'Project Three', description: 'Check back for something cool.', icon: '🎮', tag: 'just for fun' }
  ];

  const contactLinks = [
    { label: 'GitHub', href: 'https://github.com/your-username', icon: githubIcon },
    { label: 'LinkedIn', href: 'https://www.linkedin.com/in/your-username', icon: linkedinIcon },
    { label: 'Email Me', href: 'mailto:you@example.com', icon: emailIcon }
  ];
</script>

<svelte:head>
  <title>~* Haleigh's Personal Page *~</title>
  <meta name="description" content="Haleigh's Website" />
  <meta name="theme-color" content="#6c43c0" />
</svelte:head>

<div class="desktop">
  <div class="sparkles" aria-hidden="true">✦　·　✧　·　✦　·　✧</div>

  <main class="window" id="top">
    <div class="titlebar">
      <div class="window-title"><span class="cat-icon">🐈</span> Haleigh's Page</div>
      <div class="window-controls" aria-hidden="true">
        <span>−</span><span>□</span><span class="close">×</span>
      </div>
    </div>

    <nav class="menu" aria-label="Main navigation">
      <a href="#top"><u>H</u>ome</a>
      <a href="#about"><u>A</u>bout Me</a>
      <a href="#projects"><u>P</u>rojects</a>
      <a href={resumeHref} target="_blank" rel="noreferrer"><u>R</u>esume</a>
      <a href="#contact"><u>C</u>ontact</a>
    </nav>

    <div class="addressbar">
      <span class="address-label">Address</span>
      <div class="address-field"><span>🌐</span> https://haleigh.dev/home.html</div>
      <span class="go">➜ Go</span>
    </div>


    <div class="site-layout">
      <aside class="sidebar">
        <section class="panel profile-panel">
          <div class="panel-heading">User Profile</div>
          <div class="panel-body">
            <div class="avatar-wrap">
              <img src={tinaPhoto} alt="Tina the cat looking very cute" />
              <span class="online-dot"></span>
            </div>
            <h2>Haleigh</h2>
            <p class="handle">@haleighrenfroe</p>
            <p class="online">● ONLINE</p>
            <div class="mood"><strong>Mood:</strong> coding :3</div>
          </div>
        </section>

        <section class="panel nav-panel">
          <div class="panel-heading">Quick Links</div>
          <div class="panel-body quick-links">
            <a href="#about">🐾 About Me</a>
            <a href="#projects">💿 My Projects</a>
            <a href={resumeHref} target="_blank" rel="noreferrer">📄 My Resume</a>
            <a href="#contact">✉ Send a Message</a>
          </div>
        </section>

        <section class="panel tiny-panel">
          <div class="panel-heading">Currently...</div>
          <div class="panel-body">
            <p>🎧 listening to music</p>
            <p>💻 writing some code</p>
            <p>🐈 bothering Tina</p>
          </div>
        </section>

        <div class="counter">
          <span>You are visitor</span>
          <strong>0001337</strong>
        </div>
      </aside>

      <div class="content">
        <section class="hero" aria-labelledby="intro-title">
          <div class="hero-copy">
            <p class="kicker">HELLO, INTERNET!</p>
            <h1 id="intro-title">I'm <span>Haleigh!</span></h1>
            <p class="tagline">software engineer | chill person | robloxian</p>
            <p class="welcome-copy">
              Welcome to my personal website! I write software for space systems, I
              like studying digital forensics, and I love learning new things in technology. :)
            </p>
            <div class="hero-actions">
              <a class="aero-button primary" href="#projects">View my cool stuff</a>
              <a class="aero-button" href="#about">Meet me &amp; Tina</a>
            </div>
          </div>
          <div class="sticker" aria-hidden="true">
            <span class="ears">▲　▲</span>
            <span class="face">=＾● ⋏ ●＾=</span>
            <span class="sticker-text">WELCOME!</span>
          </div>
        </section>

        <div class="divider"><span>✦</span><span>✦</span><span>✦</span></div>

        <section class="web-section" id="about" aria-labelledby="about-title">
          <div class="section-titlebar">
            <h2 id="about-title"><span>👤</span> about_me.txt</h2>
            <span>− □ ×</span>
          </div>
          <div class="section-window about-grid">
            <div class="about-copy">
              <p class="big-intro">Hey there! Thanks for stopping by ♡</p>
              <p>
                I graduated from Morehead State University in 2026 with a degree in Computer Science.
                I now work at MSU as a <strong>Space Systems Software Engineer</strong>—which is every bit
                as cool as it sounds!
              </p>
              <p>
                When I'm away from the keyboard, I play drums and bass, spend time with my family,
                hang out with my cat Tina, and play video games with my friends.
              </p>
              <div class="favorites">
                <span>💜 purple things</span><span>🎵 loud music</span><span>🚀 space</span><span>🐈 cats (obviously)</span>
              </div>
            </div>
            <figure class="photo-card">
              <div class="tape" aria-hidden="true"></div>
              <img src={tinaPhoto} alt="Haleigh's cat Tina" />
              <figcaption>me &amp; my supervisor, Tina ♥</figcaption>
            </figure>
          </div>
        </section>

        <section class="web-section" id="projects" aria-labelledby="projects-title">
          <div class="section-titlebar">
            <h2 id="projects-title"><span>📁</span> C:\Haleigh\Cool Stuff</h2>
            <span>− □ ×</span>
          </div>
          <div class="section-window projects-window">
            <div class="folder-toolbar"><span>← Back</span><span>🔍 Search</span><span>▦ Views</span></div>
            <p class="folder-help">Choose an item to view its details:</p>
            <div class="project-grid">
              {#each projects as project}
                <article class="project-card">
                  <div class="project-icon">{project.icon}</div>
                  <div>
                    <h3>{project.title}</h3>
                    <span class="tag">{project.tag}</span>
                    <p>{project.description}</p>
                  </div>
                </article>
              {/each}
            </div>
          </div>
        </section>

        <section class="web-section" id="contact" aria-labelledby="contact-title">
          <div class="section-titlebar">
            <h2 id="contact-title"><span>✉️</span> New Message</h2>
            <span>− □ ×</span>
          </div>
          <div class="section-window contact-window">
            <div>
              <p class="big-intro">Let's keep in touch!</p>
              <p>Find me elsewhere on the web, send me an email, or take a peek at my resume.</p>
            </div>
            <div class="contact-links" aria-label="Contact links">
              {#each contactLinks as link}
                <a href={link.href}>
                  <span class="contact-icon"><img src={link.icon} alt="" aria-hidden="true" /></span>
                  <span>{link.label}</span>
                </a>
              {/each}
              <a href={resumeHref} target="_blank" rel="noreferrer">
                <span class="contact-icon"><img src={documentIcon} alt="" aria-hidden="true" /></span>
                <span>Resume</span>
              </a>
            </div>
          </div>
        </section>
      </div>
    </div>

    <footer class="statusbar">
      <span>🌐 Internet</span>
      <span class="footer-center">Made with 💜, HTML &amp; too much nostalgia</span>
      <span>100% ▰</span>
    </footer>
  </main>

  <p class="copyright">© 2026 Haleigh Renfroe · No cats were bothered in the making of this website</p>
</div>

<style>
  :global(*) { box-sizing: border-box; }
  :global(html) { scroll-behavior: smooth; }
  :global(body) {
    margin: 0;
    color: #271844;
    background-color: #1b0d3d;
    background-image:
      radial-gradient(circle at 50% 0%, rgba(174, 120, 255, .55), transparent 42rem),
      linear-gradient(45deg, rgba(255,255,255,.045) 25%, transparent 25%, transparent 75%, rgba(255,255,255,.045) 75%),
      linear-gradient(45deg, rgba(255,255,255,.045) 25%, transparent 25%, transparent 75%, rgba(255,255,255,.045) 75%);
    background-position: 0 0, 0 0, 8px 8px;
    background-size: auto, 16px 16px, 16px 16px;
    font-family: Tahoma, Verdana, "Segoe UI", sans-serif;
  }
  :global(a:focus-visible) { outline: 3px solid #ffdc5e; outline-offset: 2px; }

  .desktop { min-height: 100vh; padding: 34px 18px 24px; position: relative; overflow: hidden; }
  .desktop::before, .desktop::after {
    content: ''; position: fixed; z-index: -1; border-radius: 50%; filter: blur(2px); opacity: .5;
  }
  .desktop::before { width: 300px; height: 300px; right: -80px; top: 12%; background: radial-gradient(circle, #bba4ff, transparent 67%); }
  .desktop::after { width: 250px; height: 250px; left: -80px; bottom: 5%; background: radial-gradient(circle, #6e52d0, transparent 70%); }
  .sparkles { position: absolute; top: 9px; left: 0; width: 100%; color: #d9c9ff; text-align: center; letter-spacing: 2.5vw; opacity: .8; }

  .window {
    width: min(1120px, 100%); margin: 0 auto; overflow: hidden; border: 1px solid #cdc5dd; border-radius: 9px;
    background: #f6f1fc; box-shadow: 0 0 0 3px rgba(255,255,255,.25), 0 22px 70px #090319;
  }
  .titlebar {
    min-height: 45px; display: flex; align-items: center; justify-content: space-between; padding-left: 13px;
    color: white; text-shadow: 0 1px 2px #321468; background: linear-gradient(#c8b3f8 0, #8e6ed4 11%, #6241af 50%, #53369d 51%, #8162c3 100%);
    border-bottom: 1px solid #3b247a; box-shadow: inset 0 1px rgba(255,255,255,.75);
  }
  .window-title { font-weight: 700; font-size: .92rem; }
  .cat-icon { display: inline-block; padding-right: 5px; filter: drop-shadow(0 1px white); }
  .window-controls { height: 100%; display: flex; align-self: flex-start; margin-right: 7px; }
  .window-controls span { width: 46px; height: 27px; display: grid; place-items: center; border: 1px solid rgba(255,255,255,.35); border-top: 0; border-radius: 0 0 3px 3px; background: linear-gradient(rgba(255,255,255,.3), rgba(28,5,69,.22)); font-size: 1rem; }
  .window-controls .close { background: linear-gradient(#e99499, #ae2e38 55%, #db6268); }

  .menu { display: flex; gap: 2px; padding: 5px 10px; border-bottom: 1px solid #c1b8cb; background: #f2eef5; }
  .menu a { padding: 5px 10px; border-radius: 3px; color: #241934; font-size: .82rem; text-decoration: none; }
  .menu a:hover { background: #ded2f2; }
  .addressbar { display: flex; align-items: center; gap: 7px; padding: 6px 10px; border-bottom: 1px solid #aaa2b5; background: linear-gradient(#fafafa, #ddd9e1); font-size: .75rem; }
  .address-label { color: #544b60; }
  .address-field { flex: 1; padding: 5px 8px; border: 1px solid #9c96a4; background: white; box-shadow: inset 1px 1px 2px #ddd; color: #4f356e; }
  .go { padding-right: 5px; }
  @keyframes scroll { from { transform: translateX(70%); } to { transform: translateX(-100%); } }

  .site-layout { display: grid; grid-template-columns: 210px minmax(0, 1fr); gap: 18px; padding: 18px; background: linear-gradient(135deg, #ece3fb, #faf8fd 45%, #e5d9f5); }
  .sidebar { display: flex; flex-direction: column; gap: 13px; }
  .panel { overflow: hidden; border: 1px solid #8667b6; border-radius: 5px; background: #fff; box-shadow: 2px 3px 0 rgba(59,29,103,.12); }
  .panel-heading, .section-titlebar { color: white; text-shadow: 0 1px #311963; background: linear-gradient(#a88bdc, #6746ad 55%, #7858bb); }
  .panel-heading { padding: 7px 9px; font-size: .78rem; font-weight: bold; letter-spacing: .02em; }
  .panel-body { padding: 11px; }
  .profile-panel .panel-body { text-align: center; background: linear-gradient(#fff, #f1e9fc); }
  .avatar-wrap { position: relative; width: 122px; height: 122px; margin: 2px auto 9px; padding: 4px; border: 1px solid #9b7cc2; background: white; box-shadow: 0 0 0 3px #e5d8f7; }
  .avatar-wrap img { width: 100%; height: 100%; display: block; object-fit: cover; }
  .online-dot { position: absolute; right: -3px; bottom: -3px; width: 18px; height: 18px; border: 3px solid white; border-radius: 50%; background: #52bc36; }
  .profile-panel h2 { margin: 0; color: #593694; font: bold 1.3rem Georgia, serif; }
  .handle { margin: 2px 0 7px; color: #836d9d; font-size: .72rem; }
  .online { margin: 0; color: #398129; font-size: .65rem; font-weight: bold; }
  .mood { margin-top: 9px; padding: 6px; border: 1px dashed #c5acd9; background: #fff; color: #5c4b70; font: .72rem "Courier New", monospace; }
  .quick-links { padding: 5px; }
  .quick-links a { display: block; padding: 8px 7px; border-bottom: 1px dotted #c6b6d9; color: #523286; font-size: .76rem; font-weight: bold; text-decoration: none; }
  .quick-links a:last-child { border: 0; }
  .quick-links a:hover { padding-left: 11px; color: #9b238d; background: #f5edff; }
  .tiny-panel p { margin: 0 0 6px; font-size: .69rem; }
  .tiny-panel p:last-child { margin-bottom: 0; }
  .counter { padding: 7px; border: 1px solid #7356a3; background: #dcd0ec; text-align: center; font-size: .64rem; }
  .counter span { display: block; margin-bottom: 4px; }
  .counter strong { padding: 2px 5px; color: #75ff7d; background: #160e1f; font: 1rem "Courier New", monospace; letter-spacing: 2px; }

  .content { min-width: 0; }
  .hero { min-height: 340px; display: grid; grid-template-columns: minmax(0,1fr) 225px; align-items: center; gap: 25px; padding: 32px; border: 1px solid #a990c5; border-radius: 7px; background: radial-gradient(circle at 85% 20%, rgba(255,255,255,.85), transparent 32%), linear-gradient(135deg, #fff, #eee2fc 55%, #cbb3ed); box-shadow: inset 0 0 22px white, 3px 4px 0 rgba(78,43,123,.14); position: relative; overflow: hidden; }
  .hero::after { content: '✦'; position: absolute; right: 44%; top: 18px; color: #b893e2; font-size: 2rem; transform: rotate(15deg); }
  .kicker { margin: 0 0 7px; color: #8b43a0; font: bold .75rem "Courier New", monospace; letter-spacing: .18em; }
  h1 { margin: 0; color: #281540; font: bold clamp(2.7rem, 6vw, 5rem)/.9 Georgia, serif; letter-spacing: -.05em; text-shadow: 2px 2px white; }
  h1 span { color: #7947bd; font-style: italic; }
  .tagline { margin: 12px 0 18px; color: #754e96; font: bold .74rem "Courier New", monospace; }
  .welcome-copy { max-width: 550px; margin: 0; color: #4c3c58; font-size: .91rem; line-height: 1.6; }
  .hero-actions { display: flex; flex-wrap: wrap; gap: 9px; margin-top: 21px; }
  .aero-button { min-height: 34px; display: inline-flex; align-items: center; padding: 0 14px; border: 1px solid #796493; border-radius: 4px; color: #332744; background: linear-gradient(#fff, #e4daec 50%, #ccc0d8 51%, #eee8f3); box-shadow: inset 0 0 0 1px white, 0 1px 2px #aaa; font-size: .76rem; font-weight: bold; text-decoration: none; }
  .aero-button.primary { border-color: #5c3492; color: white; text-shadow: 0 1px #49217b; background: linear-gradient(#a783d2, #8152b9 50%, #6d3daa 51%, #9b71c8); }
  .aero-button:hover { filter: brightness(1.08); box-shadow: 0 0 8px #9871cb; }
  .sticker { width: 200px; height: 200px; display: flex; flex-direction: column; align-items: center; justify-content: center; transform: rotate(3deg); border: 4px solid #fff; border-radius: 50%; color: #4d2a73; background: radial-gradient(circle at 35% 25%, white, #e9d5ff 65%, #b68cde); box-shadow: 0 5px 15px rgba(52,21,83,.28), inset 0 0 0 2px #9e73ca; text-align: center; }
  .ears { margin-bottom: -7px; font-size: 1.25rem; }
  .face { font: bold 1.25rem "Courier New", monospace; white-space: nowrap; }
  .sticker-text { margin-top: 17px; padding: 4px 9px; transform: rotate(-4deg); color: white; background: #8d47ab; font: bold .76rem "Courier New", monospace; }
  .divider { display: flex; align-items: center; justify-content: center; gap: 20px; margin: 20px 0; color: #9b72c4; }
  .divider::before, .divider::after { content: ''; height: 1px; flex: 1; background: linear-gradient(90deg, transparent, #ab8ec5); }
  .divider::after { background: linear-gradient(90deg, #ab8ec5, transparent); }

  .web-section { scroll-margin-top: 15px; margin-bottom: 22px; }
  .section-titlebar { display: flex; align-items: center; justify-content: space-between; min-height: 34px; padding: 0 10px; border: 1px solid #5c3d91; border-radius: 6px 6px 0 0; box-shadow: inset 0 1px rgba(255,255,255,.55); }
  .section-titlebar h2 { margin: 0; font-size: .78rem; }
  .section-titlebar > span { font-size: .72rem; word-spacing: 8px; }
  .section-window { border: 1px solid #927dab; border-top: 0; border-radius: 0 0 5px 5px; background: rgba(255,255,255,.92); box-shadow: 3px 4px 0 rgba(58,28,94,.12); }
  .about-grid { display: grid; grid-template-columns: minmax(0, 1fr) 205px; gap: 25px; padding: 24px; }
  .about-copy p { color: #4c4055; font-size: .82rem; line-height: 1.65; }
  .about-copy .big-intro, .contact-window .big-intro { margin: 0 0 12px; color: #703ca4; font: bold italic 1.2rem Georgia, serif; }
  .favorites { display: flex; flex-wrap: wrap; gap: 6px; margin-top: 16px; }
  .favorites span { padding: 5px 8px; border: 1px solid #d1bbeb; border-radius: 12px; color: #694792; background: #f3eaff; font-size: .68rem; }
  .photo-card { position: relative; margin: 10px 0 0; padding: 9px 9px 15px; transform: rotate(2deg); background: white; box-shadow: 2px 4px 9px #b5a8bd; }
  .photo-card img { display: block; width: 100%; aspect-ratio: 1.2; object-fit: cover; }
  .photo-card figcaption { margin-top: 9px; color: #694e73; font: .72rem "Comic Sans MS", cursive; text-align: center; }
  .tape { position: absolute; z-index: 1; top: -11px; left: 63px; width: 70px; height: 24px; transform: rotate(-5deg); background: rgba(202,184,236,.72); }

  .projects-window { overflow: hidden; }
  .folder-toolbar { display: flex; gap: 10px; padding: 7px 10px; border-bottom: 1px solid #c3b9ca; background: linear-gradient(#fff, #e7e1e9); color: #51465c; font-size: .68rem; }
  .folder-toolbar span { padding-right: 10px; border-right: 1px solid #c9c2ce; }
  .folder-help { margin: 13px 15px 5px; color: #72647d; font-size: .7rem; }
  .project-grid { display: grid; grid-template-columns: repeat(3, minmax(0,1fr)); gap: 11px; padding: 12px 15px 20px; }
  .project-card { display: grid; grid-template-columns: 46px 1fr; gap: 10px; min-height: 125px; padding: 12px; border: 1px solid #d0c3dd; border-radius: 4px; background: linear-gradient(135deg, #fff, #f5effa); }
  .project-card:hover { border-color: #9569c1; background: #eee1fb; }
  .project-icon { font-size: 2rem; filter: drop-shadow(1px 2px 1px #ccc); }
  .project-card h3 { margin: 2px 0 5px; color: #513173; font-size: .82rem; }
  .project-card p { margin: 9px 0 0; color: #6c6173; font-size: .68rem; line-height: 1.4; }
  .tag { padding: 2px 5px; border-radius: 2px; color: #6b4986; background: #e8d8f8; font-size: .57rem; }

  .contact-window { display: grid; grid-template-columns: .8fr 1.2fr; align-items: center; gap: 20px; padding: 22px; }
  .contact-window p:not(.big-intro) { margin: 0; color: #66566e; font-size: .78rem; line-height: 1.55; }
  .contact-links { display: grid; grid-template-columns: repeat(2, 1fr); gap: 8px; }
  .contact-links a { display: flex; align-items: center; gap: 8px; padding: 7px 10px; border: 1px solid #b8a6ca; border-radius: 4px; color: #513873; background: linear-gradient(#fff, #e9e1ee); font-size: .71rem; font-weight: bold; text-decoration: none; }
  .contact-links a:hover { border-color: #8e5fbd; background: #eee2fa; }
  .contact-icon { width: 25px; height: 25px; display: grid; place-items: center; border-radius: 3px; background: white; }
  .contact-icon img { width: 18px; height: 18px; object-fit: contain; }

  .statusbar { display: grid; grid-template-columns: 1fr 2fr 1fr; padding: 5px 9px; border-top: 1px solid #ada6b2; color: #514959; background: linear-gradient(#f4f2f5, #d8d4db); font-size: .65rem; }
  .statusbar span { padding: 3px 7px; border: 1px solid #c6c1ca; border-top-color: #9c969f; }
  .footer-center { text-align: center; }
  .statusbar span:last-child { text-align: right; }
  .copyright { margin: 16px auto 0; color: #d7c7ed; font: .68rem "Courier New", monospace; text-align: center; text-shadow: 0 1px #100322; }

  @media (max-width: 800px) {
    .desktop { padding: 12px 8px; }
    .site-layout { grid-template-columns: 1fr; }
    .sidebar { display: grid; grid-template-columns: 1fr 1fr; }
    .profile-panel { grid-row: span 2; }
    .counter { display: none; }
    .hero { grid-template-columns: 1fr; text-align: center; }
    .hero-copy { display: flex; flex-direction: column; align-items: center; }
    .sticker { display: none; }
    .project-grid { grid-template-columns: 1fr; }
  }
  @media (max-width: 560px) {
    .window-controls span { width: 31px; }
    .menu { overflow-x: auto; }
    .menu a { white-space: nowrap; }
    .address-label, .go { display: none; }
    .site-layout { padding: 10px; }
    .sidebar { grid-template-columns: 1fr; }
    .profile-panel { grid-row: auto; }
    .nav-panel, .tiny-panel { display: none; }
    .hero { min-height: 0; padding: 32px 18px; }
    .about-grid, .contact-window { grid-template-columns: 1fr; }
    .photo-card { max-width: 230px; margin: 12px auto; }
    .contact-links { grid-template-columns: 1fr 1fr; }
    .statusbar { grid-template-columns: 1fr 1fr; }
    .footer-center { display: none; }
  }
</style>
