<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ultimate AI Video Editor</title>
  <style>
    body {
      margin: 0;
      font-family: 'Arial', sans-serif;
      background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
      color: white;
      overflow-x: hidden;
    }

    header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 20px 50px;
      background: rgba(0, 0, 0, 0.8);
      box-shadow: 0px 5px 15px rgba(0, 0, 0, 0.3);
    }

    header h1 {
      font-size: 1.8rem;
      font-weight: bold;
      color: #66d9ef;
    }

    header nav a {
      text-decoration: none;
      color: white;
      margin: 0 15px;
      transition: color 0.3s ease;
    }

    header nav a:hover {
      color: #66d9ef;
    }

    .hero {
      text-align: center;
      padding: 100px 20px;
      background: linear-gradient(145deg, #2c5364, #203a43);
      color: white;
    }

    .hero h2 {
      font-size: 3rem;
      margin-bottom: 20px;
    }

    .hero p {
      font-size: 1.2rem;
      max-width: 600px;
      margin: 0 auto 30px auto;
    }

    .hero button {
      padding: 15px 30px;
      border: none;
      border-radius: 30px;
      background: #66d9ef;
      color: #0f2027;
      font-size: 1.1rem;
      font-weight: bold;
      cursor: pointer;
      transition: transform 0.3s ease, background 0.3s ease;
    }

    .hero button:hover {
      transform: scale(1.1);
      background: #52c4d4;
    }

    .features {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 20px;
      padding: 50px;
    }

    .feature {
      background: rgba(255, 255, 255, 0.1);
      border-radius: 15px;
      padding: 30px;
      text-align: center;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      cursor: pointer;
    }

    .feature:hover {
      transform: translateY(-10px);
      box-shadow: 0px 10px 20px rgba(0, 0, 0, 0.3);
    }

    .feature h3 {
      font-size: 1.5rem;
      margin-bottom: 10px;
    }

    .feature p {
      font-size: 1rem;
      line-height: 1.6;
    }

    footer {
      text-align: center;
      padding: 20px;
      background: rgba(0, 0, 0, 0.8);
      font-size: 0.9rem;
      color: #aaa;
    }

    footer a {
      color: #66d9ef;
      text-decoration: none;
    }

    footer a:hover {
      text-decoration: underline;
    }
  </style>
</head>
<body>
  <header>
    <h1>Ultimate AI Video Editor</h1>
    <nav>
      <a href="#">Home</a>
      <a href="#features">Features</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <section class="hero">
    <h2>Elevate Your Video Editing</h2>
    <p>Discover powerful AI tools to trim, edit, and create stunning videos with ease. No experience required!</p>
    <button>Get Started</button>
  </section>

  <section id="features" class="features">
    <div class="feature">
      <h3>Trim Video</h3>
      <p>Cut and trim videos to the perfect length effortlessly.</p>
    </div>
    <div class="feature">
      <h3>Text Overlay</h3>
      <p>Add engaging text to your videos in just a few clicks.</p>
    </div>
    <div class="feature">
      <h3>Remove Background</h3>
      <p>Erase video backgrounds seamlessly with AI precision.</p>
    </div>
    <div class="feature">
      <h3>Merge Videos</h3>
      <p>Combine multiple clips into one cohesive masterpiece.</p>
    </div>
  </section>

  <footer>
    <p>&copy; 2025 Ultimate AI Video Editor | <a href="#">Privacy Policy</a></p>
  </footer>
</body>
</html>

<div class="feature">
  <h3>Trim Video</h3>
  <p>Cut and trim videos to the perfect length effortlessly.</p>
  <button id="trim-button">Trim Now</button>
</div>
<div class="feature">
  <h3>Text Overlay</h3>
  <p>Add engaging text to your videos in just a few clicks.</p>
  <button id="overlay-button">Overlay Text</button>
</div>
<div class="feature">
  <h3>Remove Background</h3>
  <p>Erase video backgrounds seamlessly with AI precision.</p>
  <button id="background-button">Remove Background</button>
</div>
<div class="feature">
  <h3>Merge Videos</h3>
  <p>Combine multiple clips into one cohesive masterpiece.</p>
  <button id="merge-button">Merge Files</button>
</div>

