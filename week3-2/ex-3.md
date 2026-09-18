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
      --card-bg: white;
      --text: #1e293b;
      --radius: 10px;
    }

    @media (prefers-color-scheme: dark) {
      :root {
        --bg: #051a0a;
        --card-bg: #0b2a18;
        --text: #d4edda;
      }
    }

    body {
      background: var(--bg);
      color: var(--text);
      font-family: sans-serif;
      padding: 20px;
    }

    .btn {
      background: var(--primary);
      color: white;
      border: none;
      padding: 10px 20px;
      border-radius: var(--radius);
      cursor: pointer;
      transition: background 0.2s;
    }

    .btn:hover {
      background: var(--accent);
    }

    .card {
      background: var(--card-bg);
      border: 2px solid var(--accent);
      border-radius: var(--radius);
      padding: 20px;
      margin-top: 16px;
      color: var(--text);
    }
  </style>
</head>

<body>
  <button class="btn">Click Me</button>

  <div class="card">
    A themed card using CSS variables
  </div>
</body>
</html>
