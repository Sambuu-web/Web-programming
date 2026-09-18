<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    :root {
      --primary: #0f766e;
      --accent: #14b8a6;
      --bg: #f0fdfa;
      --card-bg: #ffffff;
      --text: #1e293b;
      --muted: #64748b;
      --radius: 12px;
    }

    /* Dark Mode */
    @media (prefers-color-scheme: dark) {
      :root {
        --bg: #051a0a;
        --card-bg: #0b2a18;
        --text: #d4edda;
        --muted: #a7c7b0;
      }
    }

    /* Reset */
    *,
    *::before,
    *::after {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    /* Page */
    body {
      background: var(--bg);
      color: var(--text);
      font-family: Arial, sans-serif;
      padding: 40px 24px;
      line-height: 1.5;
    }

    /* Heading */
    h1 {
      color: var(--primary);
      text-align: center;
      margin-bottom: 10px;
      font-size: 2rem;
    }

    .subtitle {
      text-align: center;
      color: var(--muted);
      margin-bottom: 30px;
    }

    /* Grid */
    .grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 20px;
      max-width: 900px;
      margin: 0 auto;
    }

    /* Tablet */
    @media (min-width: 640px) {
      .grid {
        grid-template-columns: repeat(2, 1fr);
      }
    }

    /* Desktop */
    @media (min-width: 900px) {
      .grid {
        grid-template-columns: repeat(3, 1fr);
      }
    }

    /* Skill Cards */
    .card {
      background: var(--card-bg);
      border: 2px solid var(--accent);
      border-radius: var(--radius);
      padding: 28px 24px;

      color: var(--text);
      font-size: 16px;
      font-weight: 600;

      text-align: center;

      box-shadow: 0 4px 12px rgba(15, 118, 110, 0.08);

      transition:
        transform 0.25s ease,
        box-shadow 0.25s ease,
        border-color 0.25s ease;
    }

    /* Card Hover Effect */
    .card:hover {
      transform: translateY(-6px);
      border-color: var(--primary);
      box-shadow: 0 12px 28px rgba(15, 118, 110, 0.20);
    }

    /* Icons */
    .card[data-icon]::before {
      content: attr(data-icon);
      display: block;
      font-size: 2.4rem;
      margin-bottom: 14px;

      transition: transform 0.25s ease;
    }

    .card:hover::before {
      transform: scale(1.15);
    }

    /* Description */
    .card span {
      display: block;
      margin-top: 6px;
      color: var(--muted);
      font-size: 14px;
      font-weight: 400;
    }

    /* Small Screens */
    @media (max-width: 400px) {
      body {
        padding: 30px 16px;
      }

      h1 {
        font-size: 1.7rem;
      }

      .card {
        padding: 24px 18px;
      }
    }
  </style>
</head>

<body>

  <h1>My Skills</h1>
  <p class="subtitle">Technologies and concepts I am learning</p>

  <div class="grid">

    <div class="card" data-icon="🌐">
      HTML5
      <span>Structure</span>
    </div>

    <div class="card" data-icon="🎨">
      CSS3
      <span>Styling</span>
    </div>

    <div class="card" data-icon="⚡">
      JavaScript
      <span>Behaviour</span>
    </div>

    <div class="card" data-icon="📐">
      Flexbox
      <span>1D Layout</span>
    </div>

    <div class="card" data-icon="🗂️">
      Grid
      <span>2D Layout</span>
    </div>

    <div class="card" data-icon="📱">
      Responsive Design
      <span>Any Screen</span>
    </div>

  </div>

</body>
</html>
