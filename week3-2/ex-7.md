<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Batnasan Erdenesambuu - CSS Portfolio</title>

<style>
  :root {
    --primary: #0f766e;
    --accent: #14b8a6;
    --bg: #f0fdfa;
    --card-bg: #ffffff;
    --text: #1e293b;
    --muted: #64748b;
    --radius: 14px;
  }

  @media (prefers-color-scheme: dark) {
    :root {
      --bg: #071a17;
      --card-bg: #102a26;
      --text: #e2f8f4;
      --muted: #a7c5bf;
    }
  }

  *, *::before, *::after {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  html {
    scroll-behavior: smooth;
  }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Segoe UI', Arial, sans-serif;
    line-height: 1.6;
  }

  /* Navigation */
  nav {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 100;
    background: #1e293b;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 15px 40px;
    box-shadow: 0 3px 12px rgba(0, 0, 0, 0.15);
  }

  nav span {
    color: var(--accent);
    font-weight: 700;
    font-size: 1.25rem;
  }

  nav a {
    color: #cbd5e1;
    text-decoration: none;
    margin-left: 25px;
    font-weight: 500;
    transition: color 0.2s, transform 0.2s;
  }

  nav a:hover {
    color: var(--accent);
  }

  /* Hero Animation */
  @keyframes fadeSlideIn {
    from {
      opacity: 0;
      transform: translateY(30px);
    }

    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  .hero {
    min-height: 430px;
    padding: 150px 40px 90px;
    text-align: center;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    background:
      radial-gradient(circle at top right, #99f6e4 0%, transparent 35%),
      linear-gradient(135deg, var(--bg) 0%, #ccfbf1 100%);
  }

  .hero h1 {
    font-size: clamp(2.2rem, 6vw, 3.5rem);
    color: var(--primary);
    margin-bottom: 15px;
    animation: fadeSlideIn 0.8s ease-out forwards;
  }

  .hero p {
    max-width: 700px;
    font-size: 1.1rem;
    color: var(--muted);
    animation: fadeSlideIn 0.8s ease-out 0.2s both;
  }

  .hero-button {
    margin-top: 25px;
    padding: 11px 24px;
    border-radius: 25px;
    background: var(--primary);
    color: white;
    text-decoration: none;
    font-weight: 600;
    animation: fadeSlideIn 0.8s ease-out 0.4s both;
    transition: background 0.2s, transform 0.2s;
  }

  .hero-button:hover {
    background: var(--accent);
    transform: translateY(-3px);
  }

  /* Skills Section */
  .skills-section {
    max-width: 1100px;
    margin: auto;
    padding: 40px 24px 80px;
  }

  /* Sticky Heading */
  .sticky-h2 {
    position: sticky;
    top: 65px;
    z-index: 10;
    background: var(--bg);
    color: var(--primary);
    font-size: 1.5rem;
    padding: 15px 0 12px;
    border-bottom: 3px solid var(--accent);
    margin-bottom: 25px;
  }

  .section-description {
    color: var(--muted);
    margin-bottom: 25px;
  }

  /* Responsive Grid */
  .grid {
    display: grid;
    grid-template-columns: 1fr;
    gap: 20px;
  }

  @media (min-width: 640px) {
    .grid {
      grid-template-columns: repeat(2, 1fr);
    }
  }

  @media (min-width: 900px) {
    .grid {
      grid-template-columns: repeat(3, 1fr);
    }
  }

  /* Skill Cards */
  .card {
    position: relative;
    overflow: hidden;
    border: 2px solid var(--accent);
    border-radius: var(--radius);
    padding: 25px;
    min-height: 150px;

    background: var(--card-bg);
    color: var(--text);

    font-weight: 600;
    font-size: 1.05rem;

    transition:
      transform 0.25s ease,
      box-shadow 0.25s ease,
      border-color 0.25s ease;
  }

  .card:hover {
    transform: translateY(-7px);
    border-color: var(--primary);
    box-shadow: 0 12px 30px rgba(15, 118, 110, 0.20);
  }

  .card[data-icon]::before {
    content: attr(data-icon);
    display: block;
    font-size: 2.3rem;
    margin-bottom: 12px;
  }

  .card small {
    display: block;
    margin-top: 8px;
    color: var(--muted);
    font-weight: 400;
  }

  /* Footer */
  footer {
    text-align: center;
    padding: 25px;
    background: #1e293b;
    color: #cbd5e1;
    font-size: 0.9rem;
  }

  /* Mobile Navigation */
  @media (max-width: 600px) {
    nav {
      padding: 14px 20px;
    }

    nav span {
      font-size: 1rem;
    }

    nav a {
      margin-left: 12px;
      font-size: 0.9rem;
    }

    .hero {
      padding-left: 20px;
      padding-right: 20px;
    }

    .skills-section {
      padding-left: 18px;
      padding-right: 18px;
    }
  }
</style>
</head>

<body>

  <!-- Navigation -->
  <nav>
    <span>Batnasan Erdenesambuu</span>

    <div>
      <a href="#home">Home</a>
      <a href="#skills">Skills</a>
    </div>
  </nav>

  <!-- Hero Section -->
  <section class="hero" id="home">
    <h1>Hello, I am Batnasan Erdenesambuu</h1>

    <p>
      AI Software Engineering · Gachon University ·
      Week 3 CSS Advanced
    </p>

    <a href="#skills" class="hero-button">View My Skills</a>
  </section>

  <!-- Skills Section -->
  <section class="skills-section" id="skills">

    <h2 class="sticky-h2">My Skills</h2>

    <p class="section-description">
      Here are some of the technologies and web development skills
      I am learning and developing at Gachon University.
    </p>

    <div class="grid">

      <div class="card" data-icon="🌐">
        HTML5
        <small>Building the structure of modern websites.</small>
      </div>

      <div class="card" data-icon="🎨">
        CSS3 Advanced
        <small>Creating attractive and responsive designs.</small>
      </div>

      <div class="card" data-icon="⚡">
        JavaScript
        <small>Adding interaction and functionality to websites.</small>
      </div>

      <div class="card" data-icon="📐">
        Flexbox
        <small>Creating flexible and organized layouts.</small>
      </div>

      <div class="card" data-icon="🗂">
        CSS Grid
        <small>Designing powerful two-dimensional layouts.</small>
      </div>

      <div class="card" data-icon="📱">
        Responsive Design
        <small>Making websites work across different screen sizes.</small>
      </div>

    </div>
  </section>

  <!-- Footer -->
  <footer>
    © 2026 Batnasan Erdenesambuu · Gachon University
  </footer>

</body>
</html>
