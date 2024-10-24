<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Amar Badiger</title>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;600&family=Poppins:wght@300;700&display=swap"
      rel="stylesheet"
    />
    <style>
      body {
        margin: 0;
        padding: 0;
        font-family: "Poppins", sans-serif;
        background-color: #000;
        color: #fff;
        overflow: hidden;
        position: relative;
      }

      h1,
      h3 {
        font-family: "Montserrat", sans-serif;
        text-transform: uppercase;
      }

      h1 {
        font-weight: 700;
        font-size: 4em;
        letter-spacing: 0.1em;
        color: #00e5ff;
      }

      h3 {
        font-weight: 600;
        margin-top: 40px;
        margin-bottom: 20px;
        letter-spacing: 0.05em;
        color: #f3e600;
      }

      p {
        font-size: 1.3em;
        font-weight: 300;
        line-height: 1.6em;
      }

      .container {
        z-index: 10;
        position: relative;
        padding-top: 50px;
        text-align: center;
      }

      .particle-container {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        pointer-events: none;
        z-index: -1;
      }

      .particle {
        position: absolute;
        width: 3px;
        height: 3px;
        background-color: rgba(255, 255, 255, 0.7);
        border-radius: 50%;
        animation: moveParticles 8s linear infinite;
      }

      @keyframes moveParticles {
        from {
          transform: translateY(0) translateX(0);
          opacity: 1;
        }
        to {
          transform: translateY(100vh) translateX(calc(100vw * var(--random-x)));
          opacity: 0;
        }
      }

      .logo {
        margin: 15px;
        transition: transform 0.5s, box-shadow 0.5s;
      }

      .logo:hover {
        transform: translateY(-10px) rotate(5deg) scale(1.1);
      }

      .logos {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-wrap: wrap;
        gap: 20px;
      }

      .neon-button {
        display: inline-block;
        padding: 10px 30px;
        margin-top: 30px;
        border-radius: 5px;
        font-size: 1.2em;
        color: #fff;
        text-decoration: none;
        background-color: #1a1a1a;
        border: 2px solid #00e5ff;
        transition: background-color 0.5s ease, box-shadow 0.5s ease;
      }

      .neon-button:hover {
        background-color: #00e5ff;
        color: #000;
      }

      .stats img {
        margin-top: 20px;
      }
    </style>
  </head>
  <body>
    <div class="particle-container">
      <!-- Generate small, continuously flowing particles -->
      <script>
        const particleContainer = document.querySelector(".particle-container");
        for (let i = 0; i < 150; i++) {
          const particle = document.createElement("div");
          particle.classList.add("particle");
          particle.style.left = Math.random() * 100 + "vw";
          particle.style.top = Math.random() * 100 + "vh";
          particle.style.setProperty("--random-x", Math.random());
          particleContainer.appendChild(particle);
        }
      </script>
    </div>

    <div class="container">
      <h1>Hello there 👋, I'm Amar Badiger!</h1>
      <h3>👨‍💻 About Me</h3>
      <p>
        I'm a passionate Full Stack Developer from India 🌍<br /><br />
        - 🔭 Currently working on Full Stack MERN projects and exploring backend
        development.<br />
        - 📚 Constantly learning and expanding my skills in Java and the MERN
        stack.<br />
        - 🌱 Actively improving my understanding of React, Node.js, and
        MongoDB.<br />
        - ⚡ When I'm not coding, you can find me working out, meditating, or
        diving into the latest tech trends.
      </p>

      <h3>🛠 Languages and Tools</h3>
      <div class="logos">
        <img
          src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg"
          height="40"
          alt="javascript logo"
          class="logo"
        />
        <img
          src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original-wordmark.svg"
          height="40"
          alt="react logo"
          class="logo"
        />
        <img
          src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original-wordmark.svg"
          height="40"
          alt="nodejs logo"
          class="logo"
        />
        <img
          src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/express/express-original-wordmark.svg"
          height="40"
          alt="express logo"
          class="logo"
        />
        <img
          src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original-wordmark.svg"
          height="40"
          alt="mongodb logo"
          class="logo"
        />
        <img
          src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original-wordmark.svg"
          height="40"
          alt="java logo"
          class="logo"
        />
        <img
          src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bootstrap/bootstrap-plain.svg"
          height="40"
          alt="bootstrap logo"
          class="logo"
        />
        <img
          src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original-wordmark.svg"
          height="40"
          alt="git logo"
          class="logo"
        />
        <img
          src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg"
          height="40"
          alt="vscode logo"
          class="logo"
        />
      </div>

      <h3>🔥 My Stats:</h3>
      <div class="stats">
        <img
          src="https://streak-stats.demolab.com?user=amarbadiger&locale=en&mode=daily&theme=dark&hide_border=false&border_radius=5&order=3"
          height="220"
          alt="streak graph"
        />
      </div>

      <a href="#" class="neon-button">Get in Touch</a>
    </div>
  </body>
</html>
