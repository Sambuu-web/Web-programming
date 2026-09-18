<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    /* Reset */
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
      scroll-padding-top: 80px;
    }

    body {
      font-family: Arial, sans-serif;
      color: #1e293b;
      line-height: 1.6;
    }

    /* Fixed Navigation */
    .nav {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;

      height: 70px;
      padding: 0 32px;

      background: #1e293b;

      display: flex;
      justify-content: space-between;
      align-items: center;

      z-index: 1000;

      box-shadow: 0 2px 10px rgba(0, 0, 0, 0.15);
    }

    /* Logo */
    .nav-logo {
      color: #14b8a6;
      font-size: 1.4rem;
      font-weight: 700;
      text-decoration: none;

      transition: color 0.2s ease;
    }

    .nav-logo:hover {
      color: #5eead4;
    }

    /* Navigation Links */
    .nav-links {
      display: flex;
      gap: 24px;
    }

    .nav-links a {
      color: #cbd5e1;
      text-decoration: none;

      font-size: 0.95rem;
      font-weight: 500;

      padding: 8px 4px;

      transition:
        color 0.2s ease,
        transform 0.2s ease;
    }

    .nav-links a:hover {
      color: #14b8a6;
      transform: translateY(-2px);
    }

    /* Main Content */
    .content {
      padding-top: 70px;
    }

    /* Sections */
    .section {
      min-height: 350px;
      padding: 60px 40px;

      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;

      text-align: center;
      font-size: 18px;
    }

    .section h2 {
      margin-bottom: 12px;
      font-size: 2rem;
    }

    .section p {
      max-width: 600px;
      font-size: 1rem;
    }

    /* Section Backgrounds */
    #s1 {
      background: #f0fdfa;
    }

    #s2 {
      background: #ccfbf1;
    }

    #s3 {
      background: #99f6e4;
    }

    /* Mobile Design */
    @media (max-width: 600px) {
      .nav {
        padding: 0 16px;
      }

      .nav-logo {
        font-size: 1.2rem;
      }

      .nav-links {
        gap: 10px;
      }

      .nav-links a {
        font-size: 0.8rem;
      }

      .section {
        min-height: 300px;
        padding: 40px 20px;
      }

      .section h2 {
        font-size: 1.6rem;
      }
    }
  </style>
</head>

<body>

  <!-- Navigation Bar -->
  <nav class="nav">

    <a href="#s1" class="nav-logo">
      WebPro
    </a>

    <div class="nav-links">
      <a href="#s1">Home</a>
      <a href="#s2">Topics</a>
      <a href="#s3">Quiz</a>
    </div>

  </nav>

  <!-- Page Content -->
  <main class="content">

    <section class="section" id="s1">
      <h2>Home</h2>
      <p>
        Welcome to WebPro! Scroll down to explore different web development topics.
      </p>
    </section>

    <section class="section" id="s2">
      <h2>Topics</h2>
      <p>
        Learn about HTML, CSS, JavaScript, Flexbox, Grid, and responsive design.
      </p>
    </section>

    <section class="section" id="s3">
      <h2>Quiz</h2>
      <p>
        Test your knowledge of web development with our quiz!
      </p>
    </section>

  </main>

</body>
</html>
