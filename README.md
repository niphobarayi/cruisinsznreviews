<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>thebloomnote.fm</title>

  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Quicksand:wght@400;600&display=swap" rel="stylesheet" />

  <style>
    /* --- Colors (Poolsuite-inspired palette) --- */
    :root {
      --coral: #ff6b6b;
      --pool-blue: #5ddfd3;
      --sunset-yellow: #fff3a3;
      --cream: #fffaf0;
      --ocean-blue: #2364aa;
      --text-purple: #8a4fff;
      --soft-purple: #a87ee9;
      --shadow-pink: rgba(255, 107, 107, 0.25);
    }

    /* --- Reset and base --- */
    body {
      margin: 0;
      padding: 0;
      font-family: 'Quicksand', sans-serif;
      background: linear-gradient(145deg, var(--cream), #ffe0d3);
      background-attachment: fixed;
      color: var(--ocean-blue);
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }

    /* --- Header --- */
    header {
      font-family: 'Pacifico', cursive;
      font-size: 3rem;
      text-align: center;
      padding: 30px 10px 15px;
      color: var(--coral);
      text-shadow: 0 2px 8px var(--shadow-pink);
      user-select: none;
    }

    /* --- Navigation --- */
    nav {
      background-color: var(--cream);
      padding: 10px 0;
      text-align: center;
      border-bottom: 2px solid var(--pool-blue);
      box-shadow: 0 2px 8px var(--shadow-pink);
      user-select: none;
    }

    nav a {
      font-weight: 600;
      font-size: 1.1rem;
      color: var(--pool-blue);
      margin: 0 18px;
      text-decoration: none;
      transition: color 0.3s ease;
      letter-spacing: 0.04em;
    }

    nav a:hover,
    nav a:focus {
      color: var(--coral);
      text-decoration: underline;
    }

    /* --- Main container --- */
    .container {
      flex: 1;
      max-width: 1200px;
      margin: 40px auto 120px;
      padding: 0 20px;
    }

    /* --- Album Grid --- */
    .album-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
      gap: 30px;
    }

    /* --- Album Cards --- */
    .album-item {
      background: var(--cream);
      border-radius: 16px;
      overflow: hidden;
      box-shadow:
        0 4px 10px rgba(37, 150, 190, 0.12),
        0 1px 3px rgba(37, 150, 190, 0.08);
      transition: transform 0.25s ease, box-shadow 0.25s ease;
      cursor: pointer;
    }

    .album-item:hover {
      transform: scale(1.06);
      box-shadow:
        0 8px 20px rgba(255, 107, 107, 0.3),
        0 3px 6px rgba(255, 107, 107, 0.25);
    }

    .album-item img {
      display: block;
      width: 100%;
      height: auto;
      border-bottom: 6px solid var(--coral);
      transition: filter 0.3s ease;
      border-radius: 16px 16px 0 0;
    }

    .album-item:hover img {
      filter: brightness(1.1);
    }

    /* --- Album Info --- */
    .album-info {
      padding: 14px 12px 20px;
      text-align: center;
    }

    .album-title {
      font-size: 1.1rem;
      font-weight: 700;
      color: var(--pool-blue);
      margin-bottom: 6px;
      letter-spacing: 0.02em;
    }

    .album-details {
      font-size: 0.85rem;
      color: var(--soft-purple);
      margin-bottom: 8px;
    }

    /* --- Score Badge --- */
    .score-badge {
      display: inline-block;
      background: linear-gradient(45deg, var(--coral), var(--sunset-yellow));
      color: var(--ocean-blue);
      font-weight: 700;
      padding: 5px 14px;
      font-size: 0.9rem;
      border-radius: 999px;
      box-shadow: 0 0 10px var(--coral);
      user-select: none;
      letter-spacing: 0.05em;
    }

    /* --- Footer --- */
    footer {
      background-color: var(--cream);
      color: var(--pool-blue);
      text-align: center;
      padding: 18px 10px;
      font-size: 0.9rem;
      font-weight: 500;
      border-top: 1px solid var(--pool-blue);
      box-shadow: 0 -2px 6px var(--shadow-pink);
      user-select: none;
      position: fixed;
      bottom: 0;
      width: 100%;
      z-index: 10;
    }

    /* --- Responsive --- */
    @media (max-width: 600px) {
      header {
        font-size: 2.25rem;
        padding: 24px 10px 12px;
      }
      nav a {
        margin: 0 12px;
        font-size: 1rem;
      }
    }
  </style>
</head>
<body>

  <header>
    ☀️ thebloomnote.fm 🌴
  </header>

  <nav>
    <a href="#">Albums</a>
    <a href="#">Reviews</a>
    <a href="#">Lists</a>
    <a href="#">Likes</a>
    <a href="#">Library</a>
  </nav>

  <div class="container">
    <div class="album-grid">

      <!-- Men I Trust -->
      <div class="album-item" tabindex="0">
        <img src="https://upload.wikimedia.org/wikipedia/en/2/25/Men_I_Trust_-_Oncle_Jazz.png" alt="Men I Trust - Oncle Jazz" />
        <div class="album-info">
          <div class="album-title">Men I Trust</div>
          <div class="album-details">Oncle Jazz · LP · 2019</div>
          <div class="score-badge">90</div>
        </div>
      </div>

      <!-- Lauryn Hill -->
      <div class="album-item" tabindex="0">
        <img src="https://upload.wikimedia.org/wikipedia/en/0/0b/LaurynHillTheMiseducationofLaurynHillalbumcover.jpg" alt="Lauryn Hill - The Miseducation of Lauryn Hill" />
        <div class="album-info">
          <div class="album-title">Lauryn Hill</div>
          <div class="album-details">The Miseducation · LP · 1998</div>
          <div class="score-badge">100</div>
        </div>
      </div>

      <!-- SZA -->
      <div class="album-item" tabindex="0">
        <img src="https://upload.wikimedia.org/wikipedia/en/7/74/SZA_-_SOS.png" alt="SZA - SOS" />
        <div class="album-info">
          <div class="album-title">SZA</div>
          <div class="album-details">SOS · LP · 2022</div>
          <div class="score-badge">92</div>
        </div>
      </div>

      <!-- Frank Ocean -->
      <div class="album-item" tabindex="0">
        <img src="https://upload.wikimedia.org/wikipedia/en/a/a0/Blonde_-_Frank_Ocean.jpeg" alt="Frank Ocean - Blonde" />
        <div class="album-info">
          <div class="album-title">Frank Ocean</div>
          <div class="album-details">Blonde · LP · 2016</div>
          <div class="score-badge">98</div>
        </div>
      </div>

      <!-- Tyler, the Creator -->
      <div class="album-item" tabindex="0">
        <img src="https://upload.wikimedia.org/wikipedia/en/7/7e/Tyler%2C_the_Creator_-_Igor.png" alt="Tyler, the Creator - IGOR" />
        <div class="album-info">
          <div class="album-title">Tyler, the Creator</div>
          <div class="album-details">IGOR · LP · 2019</div>
          <div class="score-badge">95</div>
        </div>
      </div>

      <!-- Taylor Swift -->
      <div class="album-item" tabindex="0">
        <img src="https://upload.wikimedia.org/wikipedia/en/f/f8/Taylor_Swift_-_Folklore.png" alt="Taylor Swift - Folklore" />
        <div class="album-info">
          <div class="album-title">Taylor Swift</div>
          <div class="album-details">Folklore · LP · 2020</div>
          <div class="score-badge">90</div>
        </div>
      </div>

    </div>
  </div>

  <footer>
    &copy; 2024 thebloomnote.fm | All rights reserved 🌺
  </footer>

</body>
</html>


